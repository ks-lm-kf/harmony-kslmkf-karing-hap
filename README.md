# Karing Harmony HAP

这是基于 Karing / sing-box 核心能力编译的 HarmonyOS HAP beta 发布仓库。当前仓库只用于发布已编译 HAP、版本说明和问题反馈；源码暂未放在本公开仓库，功能也还没有完全对齐上游 Karing。

注意：当前 HAP 内含由 `KaringX/sing-box` 编译得到的 `libkaringbox.so`，其上游许可证为 GPL v3 or later，并带有不得暗示与原应用存在关联的附加要求。在未同步提供对应源码、构建脚本和许可证文件前，本二进制发布不应视为已完成 GPL 合规；请勿将本仓库描述为官方 Karing 或 sing-box 发布。

使用前请确认你理解并接受下面的说明：本软件仅供学习、研究和技术参考使用，使用时必须遵守所在地法律法规、网络服务条款和相关政策；下载、导入、测试或参考的任何资源请在 24 小时内删除；因下载、安装、导入配置、联网测试、传播、修改或使用本软件产生的任何后果由使用者自行承担，与发布者无关。

## 下载

最新版本：`1.0.6-beta`

- [v1.0.6-beta Release](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/tag/v1.0.6-beta)
- [下载 karing-harmony-1.0.6-beta.hap](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/download/v1.0.6-beta/karing-harmony-1.0.6-beta.hap)
- 文件大小：`37,645,644` bytes
- SHA256：`932FEF3096BB0A7EE01516EAE09A33B2C21BEE2E938F4B3443AA13D22FB0D4CC`

历史版本：

- [v1.0.5-beta Release](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/tag/v1.0.5-beta)
- [下载 karing-harmony-1.0.5-beta.hap](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/download/v1.0.5-beta/karing-harmony-1.0.5-beta.hap)
- SHA256：`1BBF8DA187192A443FB1660534792905C4503BC3CEE7CB3D8320A4050FD1AABA`
- [v1.0.4 Release](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/tag/v1.0.4)
- [下载 karing-harmony-1.0.4.hap](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/download/v1.0.4/karing-harmony-1.0.4.hap)
- SHA256：`487B749BD177E13A368E1010ABAF9F6A15BE1A532FB4E31CE262DBFF7EDBF0ED`
- [v1.0.3 Release](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/tag/v1.0.3)
- [下载 karing-harmony-1.0.3.hap](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/download/v1.0.3/karing-harmony-1.0.3.hap)
- SHA256：`561C422D7636AB87F921FC6261F6881596AB7AE50F9876EF1635074182078959`
- [v1.0.2 Release](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/tag/v1.0.2)
- [下载 karing-harmony-1.0.2.hap](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/download/v1.0.2/karing-harmony-1.0.2.hap)
- SHA256：`2FE93FC9604EAAA1F649E70114AA40C74F260134C0D48378EAA01D4A9374A835`
- [v1.0.1 Release](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/tag/v1.0.1)
- [下载 karing-harmony-1.0.1.hap](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/download/v1.0.1/karing-harmony-1.0.1.hap)
- SHA256：`1cf7be83e0211ef490a661c9ecc633a74804bdfeba3611e9f670631ec93446a4`
- [v1.0.0-beta Release](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/releases/tag/v1.0.0-beta)

## 兼容性

- 包名：`harmony.kslmkf.karing`
- 设备：HarmonyOS 手机
- ABI：`arm64-v8a`
- `targetSdkVersion`：HarmonyOS `6.1.1(24)`
- `compatibleSdkVersion`：HarmonyOS `6.1.0(23)`
- 目标设备 API：API 23 / API 24 手机

`1.0.6-beta` 是面向手机的 arm64 HAP，不包含仅用于模拟器的 `x86_64` ABI。

## 特性

- 基于 Karing / sing-box 核心能力编译。
- 支持 HarmonyOS VPN Ability 启动 TUN。
- 支持多个代理配置或订阅同时存在，并可新增、更新、删除和切换。
- 支持导入 URL 订阅、本地配置、sing-box JSON、Clash YAML/JSON、Base64 节点列表和常见分享链接。
- 支持常见协议或格式转换：`vmess`、`vless`、`ss`、`trojan`、`hysteria`、`hysteria2/hy2`、`tuic`、`anytls`、`ssh`、`wireguard`、`socks`、`http` 等。
- 将不同订阅和节点格式统一转换为核心可识别的 sing-box 配置。
- 支持本地 `mixed` 代理端口，默认端口 `10808`。
- 支持 Clash-compatible 控制端口，默认端口 `3057`。
- 支持规则、全局、直连等运行模式。
- 支持代理组选择、批量测速、延迟排序和节点延迟颜色标识。
- 支持关闭负载均衡，当前版本默认不启用负载均衡。
- 首次启动显示使用条款，强制阅读 5 秒后才能确认；同一安装环境只需首次确认。
- 每次启动可检查公开仓库 Release 是否有新版本；发现新版本时显示更新内容并可跳转 Release 页面。
- 设置页 / 组件页显示应用、Native wrapper 和 Karing / sing-box 核心相关版本信息。
- 首页显示本机公网与代理出口的 IPv4、IPv6、国家和地区，并提供常用境外站点实时延迟与半小时速度折线图。
- 支持跟随系统、浅色、深色、主题色、自定义颜色和背景图片设置。
- 支持液态玻璃与沉浸光效，状态栏和手势导航区域采用沉浸式布局。
- 设置页支持诊断日志开关、20 MiB 自动覆盖、崩溃恢复记录、容量统计、导出和清除。

## 更新日志

完整记录见 [CHANGELOG.md](CHANGELOG.md)。

### 1.0.6-beta

- 修复订阅链接导入后核心无法启动、而直接导入单节点分享链接可以启动的问题。
- 统一记录页面、Ability、VPN 扩展、后台订阅和 Native 核心包装层日志。
- 捕获 ArkTS 未处理异常，并在进程异常终止后的下次启动补写异常退出记录。
- 日志上限为 20 MiB，写满后自动覆盖最旧内容，双层容量条显示当前占用和累计覆盖容量。
- 支持通过系统文件选择器导出 `.log` 文件，并可一键清除日志和覆盖统计。
- 保持 `compatibleSdkVersion` 为 API 23、`targetSdkVersion` 为 API 24，发布手机 arm64 HAP。

### 1.0.5-beta

- 修复深色/浅色模式下配置名称、卡片底色和系统栏显示异常，对应 issue #8。
- 修复运行时 API 长期显示离线并阻止核心启动的问题，增加 native wrapper 延迟加载和启动容错，对应 issue #9。
- 新增完整主题设置：跟随系统、浅色、深色、主题色、自定义颜色、背景图片及透明度/模糊/适配方式。
- 新增液态玻璃与沉浸光效，主要卡片支持半透明材质、背景模糊、高光和柔和阴影。
- 应用内容延伸到状态栏和手势导航区域，修复顶部与底部黑色区域，并按主题同步系统图标明暗。
- 首页网络位置、IPv4/IPv6、站点延迟、实时速度和流量统计改为读取实际运行数据。
- 保持 `compatibleSdkVersion` 为 API 23、`targetSdkVersion` 为 API 24，发布手机 arm64 HAP。

### 1.0.4-beta

- 修复 API 23 / Mate 60 Pro / Mate 70 Pro+ 首次打开可能闪退的问题：首页不再静态加载 native wrapper，主流程初始化改为分步容错。
- 增加节点地址策略设置：自动、优先 IPv4、优先 IPv6、仅 IPv4、仅 IPv6，用于双栈/IPv6 节点连接选择。
- 启动前会把所选节点地址策略写入 sing-box 出站 `domain_strategy`，运行中切换会自动重启核心生效。
- 设置页组件信息改为显示 native wrapper 由 VPN Ability 延迟加载，避免 UI 层触发核心库加载。
- 对应用商店上架问题进行说明：当前 beta 暂以 GitHub Release 侧载发布。

### 1.0.3-beta

- 修复 VPN 启动失败后核心异常但系统 VPN 标识残留的问题，核心异常时会自动关闭 VPN，避免全局断网只能重启应用恢复。
- 修复全局模式仍带默认规则分流的问题；全局模式只保留 DNS 劫持规则，普通流量统一走当前选中节点。
- 普通 VPN 规则模式补齐 IPv6 TUN 地址、IPv6 默认路由和 IPv6 DNS 劫持，减少 IPv6 流量绕过。
- DNS 共存模式支持自定义上游 DNS 代理端口，并改为“用于接入纯 DNS 代理类软件”的通用说明。
- 规则集默认国内直连规则支持编辑、删除和调整，自动更新间隔支持自定义。
- 关闭负载均衡后，运行时配置会清理负载均衡出站引用，避免节点选择后核心仍走旧策略。

### 1.0.2-beta

- 新增启动检查更新能力：启动后检查 GitHub Release，发现高版本才弹窗，并显示 Release 更新内容。
- 设置页新增软件更新卡片，支持手动检查、打开仓库和关闭启动自动检查。
- 增强代理导入兼容性，继续补齐 `vless`、`ss`、`trojan`、Clash、v2rayN 等常见订阅/分享链接转换。
- 修复代理页顶部刷新后节点列表不及时更新的问题。
- 增加批量测速、延迟排序、海外测速 URL 和超时标识，降低测速时核心卡死风险。
- 保持 `compatibleSdkVersion` 为 API 23，`targetSdkVersion` 为 API 24，面向 API 23/24 手机发布。

## 问题反馈

请使用本仓库的 [Issues](https://github.com/ks-lm-kf/harmony-kslmkf-karing-hap/issues) 提交问题。

提交问题时建议包含：

- 手机型号、HarmonyOS 版本和 API 版本。
- HAP 版本，例如 `1.0.6-beta`。
- 安装方式和是否为首次安装。
- 订阅或配置类型，例如 Clash YAML、sing-box JSON、Base64 订阅、分享链接等。
- 复现步骤、截图和必要日志。

请不要在 Issue 中公开订阅链接、UUID、token、服务器地址、证书、账号密码或其他敏感信息。提交日志前请先自行脱敏。

## 技术栈和参考链接

HarmonyOS / ArkTS / 构建：

- HarmonyOS：[https://developer.huawei.com/consumer/cn/harmonyos](https://developer.huawei.com/consumer/cn/harmonyos)
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

## 许可证合规审计

以下检查仅是基于公开仓库 LICENSE 和当前发布内容的工程合规审计，不构成法律意见。

当前公开发布 HAP 但没有同步提供对应源码和完整第三方许可证清单，存在 GPL 合规风险。尤其是 `libkaringbox.so` 来自 `KaringX/sing-box`，该项目继承上游 `SagerNet/sing-box` 的 GPL v3 or later 授权；公开分发包含该核心的二进制时，通常需要同时提供 Corresponding Source、构建/安装所需脚本、许可证文本和修改说明。

如果继续公开发布二进制，建议尽快补齐：

- 对应本 HAP 的完整可构建源码，或至少提供覆盖 GPL 组件的 Corresponding Source 和构建脚本。
- `KaringX/sing-box` / `SagerNet/sing-box` 的 LICENSE 文本和本项目修改说明。
- Go 模块依赖、ArkTS/C++/Native 组件依赖的第三方许可证清单。
- 明确声明本项目不是 Karing、sing-box、SagerNet 或 KaringX 官方发布，不使用其名称暗示关联或背书。

已检查的引用项目：

| 项目 | 用途 | 公开许可证识别 | 当前风险 |
| --- | --- | --- | --- |
| KaringX/sing-box | 实际编译为 `libkaringbox.so` 并随 HAP 分发 | GPL v3 or later + 命名/关联限制 | 高：分发二进制时需提供对应源码和许可证材料 |
| SagerNet/sing-box | KaringX/sing-box 上游 | GPL v3 or later + 命名/关联限制 | 高：同上 |
| KaringX/karing | UI/产品方向参考 | GPL v3 or later + 命名/关联限制 | 中：如复用代码或品牌表达，需满足 GPL 和命名要求 |
| google/gVisor | sing-box 构建标签启用相关能力 | Apache-2.0 | 中：需保留许可证和 NOTICE 要求 |
| quic-go/quic-go | QUIC 能力依赖 | MIT | 低：需保留版权和许可证文本 |
| refraction-networking/uTLS | TLS 指纹能力依赖 | BSD-3-Clause | 低：需保留版权、许可证和免责声明 |
| MetaCubeX/meta-rules-dat | 规则集来源链接 | GPL-3.0 | 中：如随包分发规则数据需提供对应授权材料；仅运行时下载也应保留来源说明 |
| MetaCubeX/mihomo | Clash 兼容格式参考 | MIT | 低：当前未内置其二进制 |
| 2dust/v2rayN | 分享链接格式参考 | GPL-3.0 | 低到中：当前未内置其代码；如复用代码需 GPL 合规 |
| XTLS/Xray-core | 协议/链接格式参考 | MPL-2.0 | 低到中：当前未内置其代码；如复用文件需保留 MPL 要求 |
| apernet/hysteria | 协议/链接格式参考 | MIT | 低：当前未内置其二进制 |
| tuic-protocol/tuic | 协议/链接格式参考 | GPL-3.0 | 低到中：当前未内置其代码；如复用代码需 GPL 合规 |
| trojan-gfw/trojan | 协议/链接格式参考 | GPL-3.0 | 低到中：当前未内置其代码；如复用代码需 GPL 合规 |

## 免责声明

- 本软件仅供学习、研究和技术参考使用，不提供任何网络节点、订阅服务、账号服务或绕过限制服务。
- 使用本软件时必须遵守所在国家或地区的法律法规，以及网络服务提供方的服务条款。
- 本软件不会把用户信息、订阅内容、节点配置、规则或流量统计上传到发布者服务器；用户自行添加订阅链接时，设备会向对应链接地址发起请求。
- 用户自行导入的订阅、节点、配置、规则和其他参考资源，必须确保来源合法、授权合法；如无合法授权，请在 24 小时内删除。
- 因下载、安装、导入配置、联网测试、传播、修改或使用本软件产生的任何后果，由使用者自行承担，与发布者无关。
- Beta 版本可能存在兼容性问题、功能缺失或核心启动失败风险，请自行判断是否适合在目标设备上使用。
