## 协议与软件支持

### 配置要求

本工具生成 Mihomo（Clash Meta）格式的 YAML 配置，并使用 `listeners` 实现“一节点一端口”。

推荐使用最新版 Mihomo 内核。旧版 Clash、Clash for Windows 和 Xray/V2Ray 客户端可能不支持 `listeners`，不建议直接使用。

### 本地监听协议

| 类型 | 说明 |
| --- | --- |
| `mixed` | 同一端口同时支持 HTTP 和 SOCKS5，推荐使用 |
| `socks` | SOCKS5 代理端口 |
| `http` | HTTP 代理端口 |

### 节点协议

完整 YAML 模式可以保留 Mihomo 支持的节点配置，包括：

- Shadowsocks（SS）
- VMess
- VLESS
- Trojan
- Hysteria2
- TUIC
- WireGuard
- SOCKS5
- HTTP

转换器可直接识别以下分享链接中的节点名称：

- `ss://`
- `vmess://`
- `vless://`
- `trojan://`
- `hy2://`
- `hysteria2://`

> 分享链接模式主要用于提取节点名称并生成 `listeners`。要生成完整可运行配置，建议输入完整的 Mihomo YAML 节点配置。

## 推荐软件

| 软件 | 系统 | 说明 | 官方地址 |
| --- | --- | --- | --- |
| Mihomo | Windows、Linux、macOS | 官方内核，兼容性最好，适合直接运行生成的配置 | [GitHub Releases](https://github.com/MetaCubeX/mihomo/releases) |
| Clash Verge Rev | Windows、Linux、macOS | Mihomo 图形客户端，可导入 Clash/Mihomo 配置 | [GitHub](https://github.com/clash-verge-rev/clash-verge-rev) |
| Clash Verge Rev | Windows、Linux、macOS | 官方版本下载页面 | [GitHub Releases](https://github.com/clash-verge-rev/clash-verge-rev/releases) |
| FlClash | Windows、Linux、macOS、Android | 基于 Clash Meta 的跨平台图形客户端 | [GitHub](https://github.com/chen08209/FlClash) |
| FlClash | Windows、Linux、macOS、Android | 官方版本下载页面 | [GitHub Releases](https://github.com/chen08209/FlClash/releases) |

## 推荐选择

- Windows Server 或批量多端口：推荐直接使用 **Mihomo**
- Windows 桌面：推荐 **Clash Verge Rev**
- Android、Windows、Linux、macOS 跨平台：可使用 **FlClash**
- 需要最高兼容性：优先选择最新版 **Mihomo**


Mihomo Windows 版下载后通常这样启动：
打开cmd -f 就是配置的路径,这个是同文件夹

mihomo-windows-amd64.exe -f config.yaml



粘贴最新的 Clash/Mihomo 完整配置。

根据需要添加额外 YAML 节点。

设置起始端口和监听类型。

点击“生成配置”。

复制结果或下载 config.yaml
