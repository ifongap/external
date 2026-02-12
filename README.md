# 🧪 Fong's Network Resources Lab

![数据规模](https://img.shields.io/github/repo-size/ifongap/external?label=数据规模)
![更新频率](https://img.shields.io/badge/更新频率-持续维护-brightgreen)
![开源许可](https://img.shields.io/badge/开源许可-MIT%20License-orange)
![最近更新](https://img.shields.io/badge/最近更新-2026--02--12%20UTC%2B08-blue)

🌐 **统一访问入口：** https://a.135468.xyz/

---

欢迎来到我的个人网络资源实验仓库 👋

这里目前主要维护 **广告拦截规则（Adblock）** 与 **IPTV 直播源列表**，并通过自动化流程根据上游公开资源进行**动态同步更新**。
目标是提供 **精简、稳定、可长期引用** 的外部规则与播放列表。

> ⚠️ 本仓库以个人使用场景为基础构建，筛选逻辑具有一定主观性，请根据自身需求调整使用。

---

### 🛡️ Adblock 广告拦截规则

适用于 Clash / OpenClash / Mihomo 等支持文本规则的代理工具。

- 📌 覆盖常见网页与 App 广告域名
- 🎯 偏向“有效拦截 + 不过度误杀”
- 🔄 自动合并上游规则并去重优化
- 📂 仅提供文本格式（非 YAML / 非 Rule-Set 专用格式）

#### 🔹 Clash 引用示例

```yaml
rule-providers:
  my-adblock:
    type: http
    behavior: domain
    url: https://a.135468.xyz/adblock/ad-rules.list
    path: ./ruleset/my-adblock.yaml
    interval: 86400
```

---

### 📺 IPTV 直播源（M3U）

整理并筛选后的精简直播频道列表。

* 🌍 来源于公开网络 IPTV 资源
* 🧹 定期检测与清理失效链接
* 🧠 基于规则进行分类筛选

#### 🔹 筛选策略

* ✅ 保留央视及各省级卫视频道
* ✅ 保留部分港澳台频道
* ❌ 移除购物频道
* ❌ 剔除低清晰度与高失效率源

#### 🔹 播放列表示例地址

```
https://a.135468.xyz/iptv/iptv.m3u
```

支持所有兼容 M3U 的播放器：

* VLC
* PotPlayer
* Emby / Jellyfin 插件
* 各类电视盒子播放器

---

## 🚀 使用建议

优先通过自定义域名访问资源：

```
https://a.135468.xyz/文件路径
```

优点：

* 访问更稳定
* 可自定义 CDN 与缓存策略
* 避免 `raw.githubusercontent.com` 访问受限问题

如域名暂时不可用，可使用 GitHub 原始地址备用：

```
https://raw.githubusercontent.com/ifongap/external/main/文件路径
```

---

## 🔄 更新机制

本仓库通过 GitHub Actions 自动维护：

* ⏱️ 定期拉取上游规则与 IPTV 源
* 🧹 自动清理失效或重复条目
* 🧩 规则合并与结构优化
* 🛠️ 支持手动触发更新流程

📜 查看完整更新历史：
[https://github.com/ifongap/external/commits/main](https://github.com/ifongap/external/commits/main)

---

## ⚠️ 免责声明

1. 本仓库内容仅供学习与技术研究使用。
2. IPTV 源及部分规则来自互联网公开资源，版权归原作者或原平台所有。
3. 请勿将本仓库内容用于商业用途或任何违法行为。

---

Maintained by Fong
Fong's Network Resources Lab

```
---
```
