# v1.0.4-beta

本次发布为 `1.0.4` beta 更新，面向 HarmonyOS API 23 / API 24 手机。

## 安装包

- `karing-harmony-1.0.4.hap`
- 包名：`harmony.kslmkf.karing`
- VersionName：`1.0.4`
- VersionCode：`1000004`
- ABI：`arm64-v8a`
- 文件大小：`36,450,937` bytes
- SHA256：`487B749BD177E13A368E1010ABAF9F6A15BE1A532FB4E31CE262DBFF7EDBF0ED`

## 本次更新

- 修复 API 23 / Mate 60 Pro / Mate 70 Pro+ 首次打开可能闪退的问题，对应 issue #4、#5、#6。
- 首页不再静态加载 native wrapper，核心和 native wrapper 延迟到 VPN Ability 启动时加载。
- 主流程初始化增加分步容错，避免版本信息、运行状态、自动更新检查等能力不可用时直接闪退。
- 增加节点地址策略设置：自动、优先 IPv4、优先 IPv6、仅 IPv4、仅 IPv6，对应 issue #3。
- 启动前会把所选节点地址策略写入 sing-box 出站 `domain_strategy`，用于双栈/IPv6 节点连接选择。
- 对应用商店上架问题进行说明：当前 beta 暂以 GitHub Release 侧载发布，对应 issue #7。
- 保持 `compatibleSdkVersion` 为 API 23，`targetSdkVersion` 为 API 24，面向 API 23/24 手机发布。

## 注意

本软件仅供学习、研究和技术参考。使用时须遵守当地法律法规。用户导入的订阅、节点、配置、规则和其他参考资源必须确保合法授权；如无合法授权，请在 24 小时内删除。使用产生的任何后果由使用者自行承担，与发布者无关。
