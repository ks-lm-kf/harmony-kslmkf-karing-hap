# v1.0.9-beta

本次发布为 `1.0.9-beta` 更新，面向 HarmonyOS API 23 及以上手机。订阅转换与双栈 VPN 启动路径已在 API 23/24 模拟器回归，最终 arm64 HAP 已在 API 26 真机完成代理联网验证。

## 安装包

- `karing-harmony-1.0.9-beta.hap`
- 包名：`harmony.kslmkf.karing`
- VersionName：`1.0.9-beta`
- VersionCode：`1000009`
- ABI：`arm64-v8a`
- `compatibleSdkVersion`：HarmonyOS `6.1.0(23)`
- `targetSdkVersion`：HarmonyOS `6.1.1(24)`
- 文件大小：`36,705,035` bytes
- SHA256：`3D1D3B1CE044CC784FD357C368D3FAC11D7F6E902764E9768268CEE100C95517`

## 本次更新

- 修复核心已启动但流量未进入代理、上传下载和连接数长期为零的问题，VPN 接口统一创建 IPv4/IPv6 全设备默认路由。
- 移除部分设备不兼容的动态 `vpnId`，保留 API 23 可用的 VPN 创建路径。
- 启动前清理重复 FakeIP DNS、修复 DNS 引用，并恢复 Clash API 到 `127.0.0.1:3057`。
- 删除当前配置后立即同步代理页面；订阅更新后立即刷新更新时间、状态和节点列表，失败时恢复原配置。
- 状态栏改用独立纯色背景，不叠加模糊、渐变或液态玻璃滤镜。
- API 23/24 x86_64 模拟器已完成 VLESS、Trojan、SS 订阅下载、转换、跨进程配置和双栈 VPN 启动路径回归。
- API 26 arm64 真机已验证核心 API 在线、真实上传下载与连接统计、IPv4/IPv6 代理出口、境外站点延迟以及停止后 VPN 清理。
- 保持 API 23 最低兼容、API 24 目标版本和 arm64-v8a 手机 HAP。

## 注意

本软件仅供学习、研究和技术参考。使用时须遵守当地法律法规。用户导入的订阅、节点、配置、规则和其他参考资源必须确保合法授权；如无合法授权，请在 24 小时内删除。使用产生的任何后果由使用者自行承担，与发布者无关。
