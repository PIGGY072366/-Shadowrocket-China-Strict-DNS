# Shadowrocket China Strict DNS

> Shadowrocket 严格 DNS 防旁路 + 中国大陆分区 ECS + 国内直连 / 国外代理  
> **公开分享版，不包含任何节点、UUID、密码、REALITY 私钥、Short ID 或订阅链接。**

本项目提供 7 个中国大陆区域预设 + 1 个通用配置。目标是在使用 Shadowrocket 时，尽量避免 iOS / 路由器 / 运营商的传统 DNS 旁路，同时保持中国大陆流量 `DIRECT`，境外流量 `PROXY`。

> [!IMPORTANT]
> 这不是节点订阅。使用前必须先在 Shadowrocket 中添加并选择你自己的代理节点。  
> 严格 DNS 会让 DNS 查询经代理发往加密 DNS，因此首次冷解析会增加一段代理 RTT；ECS 用来尽量改善国内 CDN 地域调度，但不能保证所有 CDN 都采用 ECS。

## 📥 选择地区

| 配置 | 适用地区 | ECS | Raw 配置 | Shadowrocket |
|---|---|---|---|---|
| 🌐 通用 | 全国/不确定地区/海外 | 无 ECS | [Raw 下载](https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-Universal.conf) | [🚀 一键导入](https://lowertop.github.io/Shadowrocket-First/redirect.html?url=shadowrocket://config/add/https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-Universal.conf) |
| 🌴 华南 | 广东、广西、海南、福建等 | 广州代表 ECS | [Raw 下载](https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-South.conf) | [🚀 一键导入](https://lowertop.github.io/Shadowrocket-First/redirect.html?url=shadowrocket://config/add/https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-South.conf) |
| 🌊 华东 | 上海、江苏、浙江、安徽、江西、山东等 | 上海代表 ECS | [Raw 下载](https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-East.conf) | [🚀 一键导入](https://lowertop.github.io/Shadowrocket-First/redirect.html?url=shadowrocket://config/add/https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-East.conf) |
| 🏯 华北 | 北京、天津、河北、山西、内蒙古等 | 北京代表 ECS | [Raw 下载](https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-North.conf) | [🚀 一键导入](https://lowertop.github.io/Shadowrocket-First/redirect.html?url=shadowrocket://config/add/https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-North.conf) |
| 🌾 华中 | 湖北、湖南、河南等 | 武汉/湖北代表 ECS | [Raw 下载](https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-Central.conf) | [🚀 一键导入](https://lowertop.github.io/Shadowrocket-First/redirect.html?url=shadowrocket://config/add/https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-Central.conf) |
| 🐼 西南 | 四川、重庆、云南、贵州、西藏等 | 成都代表 ECS | [Raw 下载](https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-Southwest.conf) | [🚀 一键导入](https://lowertop.github.io/Shadowrocket-First/redirect.html?url=shadowrocket://config/add/https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-Southwest.conf) |
| 🏔️ 西北 | 陕西、甘肃、宁夏、青海、新疆等 | 西安/陕西代表 ECS | [Raw 下载](https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-Northwest.conf) | [🚀 一键导入](https://lowertop.github.io/Shadowrocket-First/redirect.html?url=shadowrocket://config/add/https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-Northwest.conf) |
| ❄️ 东北 | 辽宁、吉林、黑龙江等 | 沈阳/辽宁代表 ECS | [Raw 下载](https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-Northeast.conf) | [🚀 一键导入](https://lowertop.github.io/Shadowrocket-First/redirect.html?url=shadowrocket://config/add/https://raw.githubusercontent.com/PIGGY072366/Shadowrocket-China-Strict-DNS/main/configs/Strict-DNS-China-Northeast.conf) |

如果不确定自己应该选哪个，先使用 **🌐 通用版**。中国大陆用户通常选择离自己所在地最近的区域版。

## 🚀 使用方法

### 方法 1：一键导入
在 iPhone / iPad 上点击上表中的 **🚀 一键导入**。Shadowrocket 支持 `shadowrocket://config/add/{url}` URL Scheme。  
如果 GitHub App / 浏览器阻止自定义 Scheme，请改用 Raw URL 导入。

### 方法 2：Raw URL 导入
1. 点击对应地区的 **Raw 下载** 并复制 URL。
2. Shadowrocket → **配置** → 右上角 `+`。
3. 粘贴 URL → 下载。
4. 点击配置 → **使用配置**。
5. 首页选择自己的节点，并将 **全域路由**设为 `配置`。

> `raw.githubusercontent.com` 在部分中国大陆网络环境下可能无法直接访问，首次导入时可能需要先确保代理可用。

## ⚙️ 推荐设置

- 设置 → 代理 → 代理类型：**None**（TUN Only）
- 隧道 → **强制路由：开启**
- 隧道 → **包括所有网络：开启**
- 隧道 → **包括本地网络：关闭**
- **UDP 转发：开启**
- 首页 → **全域路由：配置**

DNS 泄漏测试时，如启用了 iCloud Private Relay / 专用代理或 Wi‑Fi 的“限制 IP 地址跟踪”，建议临时关闭，避免第二套中继/DNS 路径干扰判断。

## 🔐 DNS 设计

地区版核心逻辑：

```ini
dns-server = https://dns.google/dns-query#proxy&ecs=<地区代表网段>&ecs-override=true
direct-dns-server = https://dns.google/dns-query#proxy&ecs=<地区代表网段>&ecs-override=true
fallback-dns-server = https://dns.google/dns-query#proxy&ecs=<地区代表网段>&ecs-override=true

dns-direct-system = false
dns-fallback-system = false
hijack-dns = :53
```

流量逻辑：

```text
中国大陆域名/IP → DIRECT
境外/Global      → PROXY
未知流量         → PROXY
```

## 🗺️ 为什么分 7 个地区

ECS 一次查询只能携带一个客户端子网提示，Shadowrocket 的 `ecs=` 是静态参数，无法根据 GPS / 蜂窝 / Wi‑Fi 自动切换省份。

因此本项目采用“区域代表点”：
- 华南 → 广州
- 华东 → 上海
- 华北 → 北京
- 华中 → 武汉 / 湖北
- 西南 → 成都
- 西北 → 西安 / 陕西
- 东北 → 沈阳 / 辽宁

具体来源见 [`ECS-SOURCES.md`](./ECS-SOURCES.md)。

## 🧱 分流与广告

规则主要来自 `blackmatrix7/ios_rule_script`，包括 LAN、BlockHttpDNS、AdvertisingLite、Hijacking、Apple、China、Global。

广告默认使用 **AdvertisingLite**，目标是降低误杀风险。本项目不启用 MITM，因此无法保证去除 YouTube 视频广告、第一方内容流广告或与正常业务共域名的广告。

## 🧪 DNS 泄漏怎么判断

不要简单理解成“出现中国 DNS = 一定泄漏”。

如果检测结果出现未经配置的本地：
- China Mobile
- China Telecom
- China Unicom
- 家庭路由器 / ISP DNS

则需要检查 TUN、强制路由和系统中继设置。

如果主要看到代理出口附近的 Google / Cloudflare 等公共递归解析器，更符合 Strict DNS 的预期。

## ⚠️ 兼容性与取舍

- 所有 DNS 经境外代理，与“冷 DNS 保持本地 10–20ms”无法同时完全满足。
- ECS 改善的是 CDN 地域提示，不能消除跨境 DNS RTT。
- 某些 App 自带 DoH / HTTPDNS，规则只能覆盖已知目标。
- IPv6 默认关闭，用于减少额外旁路变量。
- `block-quic = all-proxy` 会阻止代理目的流量使用 QUIC/UDP 443；有明确需求可自行调整。

## 🔒 分享安全

请勿上传：
- `vless://` / `vmess://` / `trojan://` 等完整节点链接
- VLESS UUID
- REALITY Private Key
- 节点二维码 / Short ID
- 机场订阅地址
- SSH 私钥 / 密码
- 面板管理员凭据

## 📂 文件结构

```text
Shadowrocket-China-Strict-DNS/
├── README.md
├── ECS-SOURCES.md
├── SHA256SUMS.txt
└── configs/
    ├── README.md
    ├── Strict-DNS-China-Universal.conf
    ├── Strict-DNS-China-South.conf
    ├── Strict-DNS-China-East.conf
    ├── Strict-DNS-China-North.conf
    ├── Strict-DNS-China-Central.conf
    ├── Strict-DNS-China-Southwest.conf
    ├── Strict-DNS-China-Northwest.conf
    └── Strict-DNS-China-Northeast.conf
```

## 📚 参考

- [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script)
- [Shadowrocket 社区手册](https://github.com/free-nodes/shadowrocket/blob/main/docs/shadowrocket_manual.md)
- [Google Public DNS - EDNS Client Subnet](https://developers.google.com/speed/public-dns/docs/ecs)
- [ECS 网段来源](./ECS-SOURCES.md)

## 📄 License

配置文本可自由修改、学习和分享。第三方规则库仍遵循各自许可证和使用条款。

---

如果这个项目对你有帮助，可以点一个 ⭐ Star。
