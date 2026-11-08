<div align="center">

<img src="logo.png" alt="EchoMusic 插件源" width="120" height="120" />

# 🔌 xhd2005 的 EchoMusic 插件源

**一个源，收录全部四大核心插件 —— 灰歌解灰与多源换源 (`v1.0.0`) + 歌曲下载与标签内嵌 (`v2.2.0`) + 每日畅听会员领取 (`v2.4.0`) + 听歌统计 (`v1.4.0`)**

[![EchoMusic](https://img.shields.io/badge/EchoMusic-%E2%89%A52.3.2%20%7C%20v2.3.3-31cfa1?style=flat-square&logo=electron&logoColor=fff)](https://github.com/hoowhoami/EchoMusic)

</div>

这是 [EchoMusic](https://github.com/hoowhoami/EchoMusic) 插件市场的**聚合插件源**，已全面适配最新 `EchoMusic v2.3.2 / v2.3.3-beta.1`。添加本仓库地址后，即可同时发现并安装下列全部插件，无需逐个添加源。

## 🚀 快速开始

在 EchoMusic → 设置 → 插件管理 → 插件市场 → **添加源**：

```text
https://github.com/xhd2005/echo-music-plugins
```

## 📦 收录插件

| 插件 | 仓库 | 说明 |
| --- | --- | --- |
| 🔓 灰歌解灰与多源换源 (`v1.0.0`) | [echo-music-unblock](https://github.com/xhd2005/echo-music-unblock) | 全链路灰歌自动解灰、低码率无损提质、底栏音源状态胶囊与手动换源中心，支持本地曲库零流量匹配、酷狗同曲异版智能换源、外部多平台音源与自定义 API 模板，内置双语 LRC 歌词兜底 |
| 🎵 歌曲下载 (`v2.2.0`) | [echo-music-download](https://github.com/xhd2005/echo-music-download) | 原生 UI 全面重构（`DetailPageSliverHeader` + `CustomTabBar`）：支持流式下载、纯 JS 内嵌 MP3 (`ID3v2.3`) / FLAC (`Vorbis + Picture`) 封面与歌词标签、同名双语 `.lrc` 导出、用户歌单/我喜欢全量增量同步、按歌单建子目录及灰歌联动解灰下载 |
| 🎁 每日畅听会员领取 (`v2.4.0`) | [echo-music-daily-vip-claim](https://github.com/xhd2005/echo-music-daily-vip-claim) | 每日领取 1 天畅听会员、概念特权升级与听歌/广告打卡；适配新版个人中心 `.profile-details` 卡片挂载、多账号 SQLite 独立账本、7 天连胜里程碑轨道、标题栏/底栏双胶囊与 `ctx.kugouVerification.request` 安全验证桥接 |
| 📊 听歌统计 (`v1.4.0`) | [echo-music-stats](https://github.com/xhd2005/echo-music-stats) | 本地听歌统计中心：SQLite `user_id` 多账号数据隔离与「当前账号 / 全部账号」视图切换、`ctx.fs` 原生目录授权直接导出 JSON/CSV、365天热力图、24小时生物钟、完播率/切歌分析与 6 大成就勋章 |

## 🔧 工作原理

本仓库根目录的 [`echo-plugins.json`](echo-plugins.json) 是插件源索引，通过每条插件的 `repo` 字段指向其独立仓库：

```json
{
  "name": "xhd2005 的 EchoMusic 插件源",
  "homepage": "https://github.com/xhd2005/echo-music-plugins",
  "plugins": [
    { "id": "echo-music-unblock",  "repo": "xhd2005/echo-music-unblock",         "tags": ["解灰", "换源", "无损提质", "双语歌词"] },
    { "id": "echo-music-download", "repo": "xhd2005/echo-music-download",        "tags": ["下载", "ID3v2", "FLAC", "歌单增量同步"] },
    { "id": "daily-vip-claim",     "repo": "xhd2005/echo-music-daily-vip-claim", "tags": ["vip", "会员", "畅听", "每日领取"] },
    { "id": "music-stats",         "repo": "xhd2005/echo-music-stats",           "tags": ["统计", "报告", "可视化", "本地"] }
  ]
}
```

- 各插件独立仓库、独立版本，互不影响
- 新增 / 更名插件时，仅需更新本仓库的索引一行

## 📄 许可证

各插件遵循其各自仓库的许可证（GPL-3.0 / MIT）。
