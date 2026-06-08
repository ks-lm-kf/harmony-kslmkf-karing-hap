# Karing Harmony HAP

这是基于 Karing / sing-box 内核能力编译的 HarmonyOS HAP beta 发布仓库。当前仓库只用于发布已编译的 HAP 文件、记录版本说明和收集问题反馈；源码暂不公开，功能也还没有完全对齐上游 Karing。后续如果没有时间继续维护，会考虑开源。

使用前请确认你理解并接受下面的说明：本软件仅供学习、研究和技术参考使用，使用时必须遵守所在地法律法规、网络服务条款和相关政策；下载、导入、测试或参考的任何资源请在 24 小时内删除；因下载、安装、导入配置、联网测试、传播、修改或使用本软件产生的任何后果由使用者自行承担，与发布者无关。

## 下载

最新版本：`1.0.2-beta`

- [v1.0.2 Release](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/tag/v1.0.2)
- [下载 karing-harmony-1.0.2.hap](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/download/v1.0.2/karing-harmony-1.0.2.hap)
- 文件大小：`37,058,622` bytes
- SHA256：`cfb4d75f3c548c1b7a396afdcf430250234efba3fb9c57095bb1528b569fd041`

历史版本：

- [v1.0.1 Release](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/tag/v1.0.1)
- [下载 karing-harmony-1.0.1.hap](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/download/v1.0.1/karing-harmony-1.0.1.hap)
- SHA256：`1cf7be83e0211ef490a661c9ecc633a74804bdfeba3611e9f670631ec93446a4`

## 兼容性

- 包名：`harmony.kslmkf.karing`
- 设备：HarmonyOS 手机
- ABI：`arm64-v8a`
- `targetSdkVersion`：HarmonyOS `6.1.1(24)`
- `compatibleSdkVersion`：HarmonyOS `6.1.0(23)`
- 目标设备 API：API 23 / API 24 手机

`1.0.2` 是面向手机的 arm64 HAP，不包含仅用于模拟器的 `x86_64` ABI。

## 特性

- 基于 Karing / sing-box 内核能力编译。
- 支持 HarmonyOS VPN Ability 启动 TUN。
- 支持多个代理配置或订阅同时存在，并可新增、更新、删除和切换。
- 支持导入 URL 订阅、本地配置、sing-box JSON、Clash YAML/JSON、Base64 节点列表和常见分享链接。
- 支持常见协议或格式转换：`vmess`、`vless`、`ss`、`trojan`、`hysteria`、`hysteria2/hy2`、`tuic`、`anytls`、`ssh`、`wireguard`、`socks`、`http` 等。
- 将不同订阅和节点格式统一转换为核心可识别的 sing-box 配置。
- 支持本地 `mixed` 代理端口，默认端口 `10808`。
- 支持 Clash-compatible 控制端口，默认端口 `3057`。
- 支持规则、全局、直连等运行模式。
- 支持代理组选择、节点测速和当前选择持久化。
- 支持关闭负载均衡，当前版本默认不启用负载均衡。
- 首次启动显示使用条款，强制阅读 5 秒后才能确认；同一安装环境只需首次确认。
- 设置页 / 组件页显示应用、Native wrapper 和 Karing / sing-box 核心相关版本信息。

## 更新记录

### 1.0.2-beta

- 发布面向手机的 `arm64-v8a` HAP，移除仅用于模拟器测试的 `x86_64` ABI。
- 保持 `targetSdkVersion` 为 `6.1.1(24)`，`compatibleSdkVersion` 为 `6.1.0(23)`。
- 面向 API 23 / API 24 手机运行场景重新发布。
- 同步版本号和组件展示为 `1.0.2`。

### 1.0.1-beta

- 恢复 `1.0.1` release 为手机 arm64 HAP。
- 修复未导入代理配置时核心不应启动的问题。
- 增加多配置 / 多订阅存在和切换能力。
- 优化订阅导入与格式转换，减少核心启动失败。
- 增加负载均衡开关，当前默认关闭。
- 修复规则 final 走向异常导致选择节点后仍无法正常联网的问题。

### 1.0.0-beta

- 初始 HarmonyOS HAP beta 版本。
- 接入 Karing / sing-box 核心能力。
- 支持 HarmonyOS VPN Ability、TUN、mixed 代理端口和 Clash-compatible 控制端口。
- 增加首次启动使用条款确认。
- 增加组件版本展示。

## 问题反馈

请使用本仓库的 [Issues](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/issues) 提交问题。

提交问题时建议包含：

- 手机型号、HarmonyOS 版本和 API 版本。
- HAP 版本，例如 `1.0.2-beta`。
- 安装方式和是否为首次安装。
- 订阅或配置类型，例如 Clash YAML、sing-box JSON、Base64 订阅、分享链接等。
- 复现步骤、截图和必要日志。

请不要在 Issue 中公开订阅链接、UUID、token、服务器地址、证书、账号密码或其他敏感信息。提交日志前请先自行脱敏。

## 技术栈和参考链接

HarmonyOS / ArkTS / 构建：

- HarmonyOS 文档：[https://developer.huawei.com/consumer/cn/harmonyos](https://developer.huawei.com/consumer/cn/harmonyos)
- DevEco Studio：[https://developer.huawei.com/consumer/cn/deveco-studio/](https://developer.huawei.com/consumer/cn/deveco-studio/)
- ArkTS：[https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/arkts-overview](https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/arkts-overview)
- ArkUI：[https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/arkui-overview](https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/arkui-overview)
- HarmonyOS N-API：[https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/napi-guidelines](https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/napi-guidelines)
- CMake：[https://cmake.org/](https://cmake.org/)
- Go：[https://go.dev/](https://go.dev/)

核心和网络能力：

- Karing：[https://github.com/KaringX/karing](https://github.com/KaringX/karing)
- KaringX / sing-box：[https://github.com/KaringX/sing-box](https://github.com/KaringX/sing-box)
- SagerNet / sing-box：[https://github.com/SagerNet/sing-box](https://github.com/SagerNet/sing-box)
- sing-box 文档：[https://sing-box.sagernet.org/](https://sing-box.sagernet.org/)
- gVisor：[https://github.com/google/gvisor](https://github.com/google/gvisor)
- quic-go：[https://github.com/quic-go/quic-go](https://github.com/quic-go/quic-go)
- WireGuard：[https://www.wireguard.com/](https://www.wireguard.com/)
- uTLS：[https://github.com/refraction-networking/utls](https://github.com/refraction-networking/utls)
- MetaCubeX meta-rules-dat：[https://github.com/MetaCubeX/meta-rules-dat](https://github.com/MetaCubeX/meta-rules-dat)

兼容格式参考：

- Clash / Mihomo 配置：[https://wiki.metacubex.one/config/](https://wiki.metacubex.one/config/)
- Mihomo：[https://github.com/MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo)
- v2rayN：[https://github.com/2dust/v2rayN](https://github.com/2dust/v2rayN)
- Xray-core：[https://github.com/XTLS/Xray-core](https://github.com/XTLS/Xray-core)
- V2Fly：[https://www.v2fly.org/](https://www.v2fly.org/)
- Hysteria：[https://github.com/apernet/hysteria](https://github.com/apernet/hysteria)
- TUIC：[https://github.com/EAimTY/tuic](https://github.com/EAimTY/tuic)
- Shadowsocks：[https://shadowsocks.org/](https://shadowsocks.org/)
- Trojan：[https://github.com/trojan-gfw/trojan](https://github.com/trojan-gfw/trojan)

## 开源协议和合规说明

- 本仓库当前只发布 HAP 文件和版本说明，源码暂不公开。
- 本项目使用或参考了多个开源项目、协议实现、文档和生态格式，上游项目版权归各自作者或组织所有。
- 各上游项目的许可协议以其原仓库 `LICENSE`、`NOTICE`、源码头和发布说明为准。
- 已检查主要引用仓库的 GitHub license 元数据：`MetaCubeX/meta-rules-dat` 为 GPL-3.0；`KaringX/karing` 和 `SagerNet/sing-box` 在 GitHub 上识别为 `NOASSERTION/Other`，请以原仓库实际许可证文件为准。
- 如果本发布包、README 或引用说明存在许可证、版权、NOTICE、源码提供方式或链接遗漏问题，请通过 Issues 提交，发布者会根据上游协议要求进行修正、补充或调整发布方式。
- 本仓库不声明拥有上游 Karing、sing-box、Clash、Mihomo、Xray、V2Ray、Shadowsocks、Trojan、Hysteria、TUIC、WireGuard 等项目的商标、名称或版权。

## 免责声明

- 本软件仅供学习、研究和技术参考使用，不提供任何网络节点、订阅服务、账号服务或绕过限制服务。
- 使用本软件时必须遵守所在国家或地区的法律法规，以及网络服务提供方的服务条款。
- 本软件不会把用户信息、订阅内容、节点配置、规则或流量统计上传到发布者服务器；用户自行添加订阅链接时，设备会向对应链接地址发起请求。
- 用户自行导入的订阅、节点、配置、规则和其他参考资源，必须确保来源合法、授权合法；如无合法授权，请在 24 小时内删除。
- 因下载、安装、导入配置、联网测试、传播、修改或使用本软件产生的任何后果，由使用者自行承担，与发布者无关。
- Beta 版本可能存在兼容性问题、功能缺失或核心启动失败风险，请自行判断是否适合在目标设备上使用。
