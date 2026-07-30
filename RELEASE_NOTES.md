# v1.0.6-beta

本次发布为 `1.0.6-beta` 更新，面向 HarmonyOS API 23 / API 24 手机。

## 安装包

- `karing-harmony-1.0.6-beta.hap`
- 包名：`harmony.kslmkf.karing`
- VersionName：`1.0.6-beta`
- VersionCode：`1000006`
- ABI：`arm64-v8a`
- `compatibleSdkVersion`：HarmonyOS `6.1.0(23)`
- `targetSdkVersion`：HarmonyOS `6.1.1(24)`
- 文件大小：`37,645,644` bytes
- SHA256：`932FEF3096BB0A7EE01516EAE09A33B2C21BEE2E938F4B3443AA13D22FB0D4CC`

## 本次更新

- 修复订阅链接导入后核心无法启动、而直接导入单节点分享链接可以启动的问题。
- 设置页新增诊断日志开关，统一记录页面、Ability、VPN 扩展、后台订阅和 Native 核心包装层日志。
- 捕获 ArkTS 未处理异常，并在进程异常终止后的下次启动补写异常退出记录。
- 日志上限为 20 MiB，写满后自动覆盖最旧内容，双层容量条显示当前占用和累计覆盖容量。
- 支持通过系统文件选择器导出普通 `.log` 文件，并可一键清除日志与覆盖统计。
- 保持 API 23 兼容、API 24 目标版本，发布手机可安装的 arm64-v8a HAP。

## 注意

本软件仅供学习、研究和技术参考。使用时须遵守当地法律法规。用户导入的订阅、节点、配置、规则和其他参考资源必须确保合法授权；如无合法授权，请在 24 小时内删除。使用产生的任何后果由使用者自行承担，与发布者无关。
