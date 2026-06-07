# Karing Harmony HAP

这是基于 Karing/sing-box 核心编译的鸿蒙系统 HAP 测试版本。当前仓库只用于发布已编译安装包和版本说明，源码暂时不开源，也尚未完全对齐上游 Karing 的全部功能；如果后续没有时间维护，可能会开源归档。

## 当前版本

- 版本：`1.0.0-beta`
- 包名：`harmony.kslmkf.karing`
- VersionCode：`1000000`
- 架构：`arm64-v8a`
- 安装包：请在 Releases 下载 `harmony-kslmkf-karing-v1.0.0-beta.hap`
- SHA256：`4769EB3C017F56F84EB5C5D4E165F458365D1060CAFE5BAF0D9A319630118EA7`

## Beta 1.0.0 首次更新

- 增加 HarmonyOS HAP 应用外壳，支持手机设备安装和启动。
- 接入 Karing/sing-box 原生核心，支持通过 HarmonyOS VPN Ability 启动 TUN。
- 首次启动显示使用条款，需要强制阅读 5 秒后才能继续使用；同一安装环境只需确认一次。
- 未导入代理配置时使用 direct-only 配置，避免空配置导致核心启动失败。
- 支持多个代理配置同时存在，可新增、切换、更新、删除。
- 支持导入订阅链接、sing-box JSON、Clash YAML/JSON、Base64 节点列表和常见分享链接。
- 支持常见协议或格式转换：`vmess`、`vless`、`ss`、`trojan`、`hysteria`、`hysteria2/hy2`、`tuic`、`anytls`、`ssh`、`wireguard`、`socks`、`http` 等。
- 支持 WorkerVless2sub 一类订阅 URL 的参数兜底转换。
- 提供本地 mixed 代理端口 `10808` 和 Clash-compatible 控制端口 `3057`。
- 设置页增加组件版本显示，包括应用版本、Native wrapper 和 Karing/sing-box 核心编译信息。

## 核心编译信息

- 运行时核心：`libkaringbox.so`
- 核心来源：`KaringX/sing-box`
- 分支：`dev-next`
- 构建提交：`73603b2-dirty`
- 编译时间标记：`KaringX/sing-box prebuilt 2026-06-07 11:07:38 arm64-v8a`
- Go 构建目标：`GOOS=android`、`GOARCH=arm64`、`CGO_ENABLED=1`
- 编译模式：`c-shared`
- 编译标签：`netgo`、`osusergo`、`with_gvisor`、`with_quic`、`with_wireguard`、`with_utls`、`with_clash_api`

## 技术栈和参考链接

运行时和构建：

- HarmonyOS：[https://developer.huawei.com/consumer/cn/harmonyos](https://developer.huawei.com/consumer/cn/harmonyos)
- DevEco Studio：[https://developer.huawei.com/consumer/cn/deveco-studio/](https://developer.huawei.com/consumer/cn/deveco-studio/)
- ArkTS：[https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/arkts-overview](https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/arkts-overview)
- ArkUI：[https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/arkui-overview](https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/arkui-overview)
- HarmonyOS N-API：[https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/napi-guidelines](https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/napi-guidelines)
- CMake：[https://cmake.org/](https://cmake.org/)
- Go：[https://go.dev/](https://go.dev/)

核心和网络能力：

- Karing：[https://github.com/KaringX/karing](https://github.com/KaringX/karing)
- KaringX/sing-box：[https://github.com/KaringX/sing-box](https://github.com/KaringX/sing-box)
- SagerNet/sing-box：[https://github.com/SagerNet/sing-box](https://github.com/SagerNet/sing-box)
- sing-box 文档：[https://sing-box.sagernet.org/](https://sing-box.sagernet.org/)
- gVisor：[https://github.com/google/gvisor](https://github.com/google/gvisor)
- quic-go：[https://github.com/quic-go/quic-go](https://github.com/quic-go/quic-go)
- WireGuard：[https://www.wireguard.com/](https://www.wireguard.com/)
- uTLS：[https://github.com/refraction-networking/utls](https://github.com/refraction-networking/utls)
- MetaCubeX meta-rules-dat：[https://github.com/MetaCubeX/meta-rules-dat](https://github.com/MetaCubeX/meta-rules-dat)

兼容格式参考：

- Clash/Mihomo 配置：[https://wiki.metacubex.one/config/](https://wiki.metacubex.one/config/)
- Mihomo：[https://github.com/MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo)
- v2rayN：[https://github.com/2dust/v2rayN](https://github.com/2dust/v2rayN)
- Xray-core：[https://github.com/XTLS/Xray-core](https://github.com/XTLS/Xray-core)
- V2Fly：[https://www.v2fly.org/](https://www.v2fly.org/)
- Hysteria：[https://github.com/apernet/hysteria](https://github.com/apernet/hysteria)
- TUIC：[https://github.com/EAimTY/tuic](https://github.com/EAimTY/tuic)
- Shadowsocks：[https://shadowsocks.org/](https://shadowsocks.org/)
- Trojan：[https://github.com/trojan-gfw/trojan](https://github.com/trojan-gfw/trojan)

## 使用说明

1. 从 Releases 下载 HAP 文件。
2. 使用支持 HAP 安装的工具安装到鸿蒙设备。
3. 第一次打开后阅读并确认使用条款。
4. 导入合法来源的订阅链接、Clash 配置、sing-box JSON 或分享链接。
5. 如网络直连不稳定，可在可用环境下使用本地 `10808` mixed 代理端口进行相关网络请求。

不同设备、系统版本、签名证书和安装策略可能不同，安装失败时请先确认设备是否允许安装调试或测试 HAP。

## 免责声明

- 本软件仅供学习、研究和技术参考使用，不提供任何网络节点、订阅服务、账号服务或绕过限制服务。
- 使用本软件时必须遵守所在国家或地区的法律法规以及网络服务条款。
- 本软件不会把信息上传到发布者服务器，也不内置统计、埋点或远程数据收集；用户自行添加订阅链接时，设备会向对应链接地址发起请求。
- 用户自行导入的订阅、节点、配置、规则和其他参考资源，必须确保来源合法、授权合法；如无合法授权，请在 24 小时内删除。
- 因下载、安装、导入配置、联网测试、传播、修改或使用本软件产生的任何后果，由使用者自行承担，与发布者无关。
- Beta 版本可能存在兼容性问题、功能缺失或核心启动失败风险，请自行判断是否适合在目标设备上使用。
- 当前版本暂时不开源，后续是否开源、维护或继续发布由发布者根据时间和维护成本决定。
