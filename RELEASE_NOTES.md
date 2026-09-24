# v1.10.0

本次发布为 `1.10.0` 更新，面向 HarmonyOS API 23 及以上手机。

## 安装包

- `karing-harmony-1.10.0.hap`
- 包名：`harmony.kslmkf.karing`
- VersionName：`1.10.0`
- VersionCode：`1010000`
- ABI：`arm64-v8a`
- `compatibleSdkVersion`：HarmonyOS `6.1.0(23)`
- `targetSdkVersion`：HarmonyOS `6.1.1(24)`
- 文件大小：`48,424,888` bytes
- SHA256：`3851336BA2604E3AA3C634A08046EBAE37C2207A98E6A666EF1C29B802342A50`

## 本次更新

- 修复配置编辑保存读取旧配置的问题，保存后同步运行配置、代理页面和节点列表。
- 修复规则、节点和负载均衡配置保存后 VPN 扩展仍读取旧运行配置的问题。
- 核心构建加入 `with_tailscale`，ARM64 与 x86_64 核心均包含真实 Tailscale endpoint 实现。
- Tailscale endpoint 可通过配置校验，并在代理页显示为 `tailscale` 节点。
- 改进 VLESS Reality 大小写识别、gRPC/WS 参数和 WebSocket early-data (`ed`) 转换。
- 当前核心不支持 XHTTP/SplitHTTP，导入时明确提示原因。
- 日志脱敏覆盖 Tailscale、WireGuard、私钥和预共享密钥字段。
- API 23/24 模拟器完成订阅导入和启动路径检查；API 26 真机完成 `1.10.0` 安装启动验证。
- 保持 API 23 最低兼容、API 24 目标版本和 arm64-v8a 手机 HAP。

## 注意

本软件仅供学习、研究和技术参考。使用时须遵守当地法律法规。用户导入的订阅、节点、配置、规则和其他参考资源必须确保合法授权；如无合法授权，请在 24 小时内删除。使用产生的任何后果由使用者自行承担，与发布者无关。
