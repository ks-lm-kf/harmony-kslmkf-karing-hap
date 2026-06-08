# v1.0.2-beta

本次发布为 `1.0.2` beta 更新，面向 HarmonyOS API 23 / API 24 手机。

## 安装包

- `karing-harmony-1.0.2.hap`
- 包名：`harmony.kslmkf.karing`
- VersionName：`1.0.2`
- VersionCode：`1000002`
- ABI：`arm64-v8a`
- 文件大小：`36,396,480` bytes
- SHA256：`2FE93FC9604EAAA1F649E70114AA40C74F260134C0D48378EAA01D4A9374A835`

## 本次更新

- 新增启动检查更新能力：启动后检查 GitHub Release，发现高版本才弹窗，并显示 Release 更新内容。
- 设置页新增软件更新卡片，支持手动检查、打开仓库和关闭启动自动检查。
- 增强代理导入兼容性，补齐 `vless`、`ss`、`trojan`、Clash、v2rayN 等常见订阅/分享链接转换。
- 修复代理页顶部刷新后节点列表不及时更新的问题。
- 增加批量测速、延迟排序、海外测速 URL 和超时标识，降低测速时核心卡死风险。
- 保持 `compatibleSdkVersion` 为 API 23，`targetSdkVersion` 为 API 24，面向 API 23/24 手机发布。

## 注意

本软件仅供学习、研究和技术参考。使用时须遵守当地法律法规。用户导入的订阅、节点、配置、规则和其他参考资源必须确保合法授权；如无合法授权，请在 24 小时内删除。使用产生的任何后果由使用者自行承担，与发布者无关。
