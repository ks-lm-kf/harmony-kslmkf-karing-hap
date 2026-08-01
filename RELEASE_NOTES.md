# v1.0.8-beta

本次发布为 `1.0.8-beta` 更新，面向 HarmonyOS API 23 及以上手机。URL 订阅启动路径已在 API 23/24 模拟器回归，最终 arm64 HAP 已在 API 26 真机安装和启动验证。

## 安装包

- `karing-harmony-1.0.8-beta.hap`
- 包名：`harmony.kslmkf.karing`
- VersionName：`1.0.8-beta`
- VersionCode：`1000008`
- ABI：`arm64-v8a`
- `compatibleSdkVersion`：HarmonyOS `6.1.0(23)`
- `targetSdkVersion`：HarmonyOS `6.1.1(24)`
- 文件大小：`36,695,090` bytes
- SHA256：`CF9E254982F5204C6C29BD05A6D3332C791FDDC28F50A6291D5867005B57CDCA`

## 本次更新

- 修复 URL 订阅配置内自带 TUN 入站时核心启动失败的问题，统一替换为 HarmonyOS VPN 所需的双栈 TUN。
- 启动前再次清洗重复 TUN、订阅携带的接口名称和无效接口地址，避免 `bind: cannot assign requested address`。
- 订阅链接和单节点分享链接统一经过转换、校验与运行配置暂存后再启动核心。
- 核心启动或停止异常时继续销毁 VPN，避免系统 VPN 标识残留和设备断网。
- API 23/24 x86_64 模拟器回归均通过，测试覆盖 URL 订阅导入、TUN 清洗、跨进程配置和 VPN Ability 启动。
- API 26 arm64 真机完成最终签名 HAP 覆盖安装、版本元数据和前台启动验证。
- 保持 API 23 最低兼容、API 24 目标版本和 arm64-v8a 手机 HAP。

## 注意

本软件仅供学习、研究和技术参考。使用时须遵守当地法律法规。用户导入的订阅、节点、配置、规则和其他参考资源必须确保合法授权；如无合法授权，请在 24 小时内删除。使用产生的任何后果由使用者自行承担，与发布者无关。
