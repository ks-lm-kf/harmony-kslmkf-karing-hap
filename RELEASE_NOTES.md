# v1.0.5-beta

本次发布为 `1.0.5-beta` 更新，面向 HarmonyOS API 23 / API 24 手机。

## 安装包

- `karing-harmony-1.0.5-beta.hap`
- 包名：`harmony.kslmkf.karing`
- VersionName：`1.0.5-beta`
- VersionCode：`1000005`
- ABI：`arm64-v8a`
- `compatibleSdkVersion`：HarmonyOS `6.1.0(23)`
- `targetSdkVersion`：HarmonyOS `6.1.1(24)`
- 文件大小：`37,084,188` bytes
- SHA256：`1BBF8DA187192A443FB1660534792905C4503BC3CEE7CB3D8320A4050FD1AABA`

## 本次更新

- 修复深色/浅色模式下配置名称、卡片底色和系统栏显示异常，对应 issue #8。
- 修复运行时 API 长期显示离线并阻止核心启动的问题，增加 native wrapper 延迟加载和启动容错，对应 issue #9。
- 新增完整主题设置及液态玻璃与沉浸光效。
- 应用内容延伸到状态栏和手势导航区域，修复顶部与底部黑色区域。
- 首页增加本机公网与代理出口 IPv4/IPv6、国家地区、境外站点延迟和半小时实时速度折线图。
- 网络位置、延迟、实时速度、上传下载、连接数和内存数据改为读取实际运行状态。
- 保持 API 23 兼容、API 24 目标版本，发布手机可安装的 arm64-v8a HAP。

## 注意

本软件仅供学习、研究和技术参考。使用时须遵守当地法律法规。用户导入的订阅、节点、配置、规则和其他参考资源必须确保合法授权；如无合法授权，请在 24 小时内删除。使用产生的任何后果由使用者自行承担，与发布者无关。
