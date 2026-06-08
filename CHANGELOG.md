# 更新日志

## 1.0.2-beta

- 新增启动检查更新能力：每次启动可检查公开仓库 Release，只有发现新版本才弹窗。
- 更新弹窗显示 Release 更新内容，并支持跳转到仓库 Release 页面。
- 设置页新增软件更新卡片，支持手动检查、打开仓库和关闭启动自动检查。
- 增强订阅和分享链接导入兼容性，继续补齐 `vless`、`ss`、`trojan`、Clash、v2rayN 等格式转换。
- 修复代理页顶部刷新后节点列表不及时更新的问题。
- 增加批量测速、延迟排序、海外测速 URL、延迟颜色和 `timeout` 标识。
- 优化批量测速并发和间隔，降低测速时核心卡死风险。
- 保持 `compatibleSdkVersion` 为 API 23，`targetSdkVersion` 为 API 24，发布手机可运行的 arm64 HAP。

## 1.0.1-beta

- 恢复 `1.0.1` release 为手机 arm64 HAP。
- 修复未导入代理配置时核心不应启动的问题。
- 增加多配置 / 多订阅存在和切换能力。
- 优化订阅导入与格式转换，减少核心启动失败。
- 增加负载均衡开关，当前默认关闭。
- 修复规则 final 走向异常导致选择节点后仍无法正常联网的问题。

## 1.0.0-beta

- 初始 HarmonyOS HAP beta 版本。
- 接入 Karing / sing-box 核心能力。
- 支持 HarmonyOS VPN Ability、TUN、mixed 代理端口和 Clash-compatible 控制端口。
- 增加首次启动使用条款确认。
- 增加组件版本展示。
