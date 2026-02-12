# 🧪 Fong's Network Resources Lab

![数据规模](https://img.shields.io/github/repo-size/ifongap/external?label=数据规模)
![更新频率](https://img.shields.io/badge/更新频率-持续维护-brightgreen)
![开源许可](https://img.shields.io/badge/开源许可-MIT%20License-orange)
![最近更新](https://img.shields.io/badge/最近更新-2026--02--12%20UTC%2B08-blue)
[![访问入口](https://img.shields.io/badge/访问入口-https://a.135468.XYZ-blueviolet)](https://a.135468.xyz)

---

欢迎来到我的个人网络资源实验仓库 👋

本仓库当前主要维护 **广告拦截规则（**Adblock Plus 格式**）** 与 ​**IPTV 直播源列表**​，并通过自动化流程与上游资源保持​**动态同步更新**​。旨在提供**精简、稳定、可长期引用**的网络配置资源。


> ⚠️ 本仓库以个人使用场景为基础构建，筛选逻辑具有一定主观性，请根据自身需求调整使用。

---

### 🛡️ Adblock 广告拦截规则

适用于**兼容 Adblock Plus 语法的浏览器广告拦截扩展**，以及 ​**支持文本规则的代理工具**​（如 Clash / OpenClash / Mihomo） ​​。

* 📌 覆盖常见网页及 App 广告域名
* 🎯 兼顾「有效拦截 + 低误杀」的平衡策略
* 🔄 自动合并上游规则，去重并移除失效冗余规则
* 📂 仅提供文本规则格式（非 YAML / 非 Rule-Set 专用格式）

#### 🔹 Clash 引用示例

```yaml
rule-providers:
  my-adblock:
    type: http
    behavior: domain
    url: https://a.135468.xyz/adblock/adblocklist.txt
    path: ./ruleset/adblock.yaml
    interval: 86400
```

---

### 📺 IPTV 直播源（M3U）

整理并筛选后的精简直播频道列表。

* 🌍 来源于公开网络 IPTV 资源
* 🧹 定期自动检测并清理失效链接
* 🧠 基于多维评估体系进行分类筛选

#### 🔹 筛选策略

✅ 保留央视及省级卫视（含直辖市、港澳台）

✅ 保留国际知名新闻、财经、体育及纪录片频道

❌ 移除购物、电竞、游戏、网络直播、剧场频道

❌ 剔除低清晰度、连接不稳的源及非中文或非英语频道


📁 分为央视频道、卫视频道、体育频道及国际频道四类

#### 🔹 播放列表示例地址

```
https://a.135468.xyz/iptv/live.m3u
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
* 规避 `raw.githubusercontent.com` 访问限制

如遇域名暂时不可用，可使用 GitHub 原始地址备用：

```
https://raw.githubusercontent.com/ifongap/external/main/文件路径
```

---

## ⚠️ 免责声明

1. 本仓库内容仅供学习与技术研究使用。
2. 部分资源来自公开网络，版权归原作者或相关平台。
3. 请勿将本仓库任何内容用于商业用途或任何违法行为。

---