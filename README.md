<div align="center">

<img src="logo.png" alt="EchoMusic 插件源" width="120" height="120" />

# 🔌 xhd2005 的 EchoMusic 插件源

**一个源，收录全部四大核心插件 —— 灰歌解灰与多源换源 (`v1.1.1`) + 歌曲下载与标签内嵌 (`v2.4.2`) + 每日畅听会员领取 (`v2.5.2`) + 听歌统计 (`v1.5.0`)**

[![EchoMusic](https://img.shields.io/badge/EchoMusic-%E2%89%A52.3.2%20%7C%20v2.3.3-31cfa1?style=flat-square&logo=electron&logoColor=fff)](https://github.com/hoowhoami/EchoMusic)

</div>

这是 [EchoMusic](https://github.com/hoowhoami/EchoMusic) 插件市场的**聚合插件源**，全部 4 款插件均已统一对齐 EchoMusic `v2.3.x` 第一方原生极简视觉规范（`PageScrollContainer` + 随主题变色 `DetailPageSliverHeader` + 原生下划线 `Tabs` + `Drawer` / `Dialog` / `Popconfirm` + 无框清爽行列表），全面适配浅色与深色模式。

## 🚀 快速开始

在 EchoMusic → 设置 → 插件管理 → 插件市场 → **添加源**：

```text
https://github.com/xhd2005/echo-music-plugins
```

## 📦 收录插件

| 插件 | 仓库 | 说明 |
| --- | --- | --- |
| 🔓 灰歌解灰与多源换源 (`v1.1.1`) | [echo-music-unblock](https://github.com/xhd2005/echo-music-unblock) | 全链路灰歌自动解灰、低码率无损提质与双语歌词兜底；主进程 `ctx.net.request` 零 CORS 硬超时链路、原生下划线 `Tabs` + `Dialog` 换源弹窗、独立「已锁定音源」管理与过期直链自动续链及一键联动下载 |
| 🎵 歌曲下载 (`v2.4.2`) | [echo-music-download](https://github.com/xhd2005/echo-music-download) | 原生极简 4 格仪表盘概览 + 3 格快捷导入卡 + 双 Tab（「正在下载 / 已下载」）；原生 ➔ 主进程直连 ➔ aria2c ➔ 解灰四级自动回退彻底告别连接超时，支持已下载双击本地播放、纯 JS MP3/FLAC 标签内嵌及双语 `.lrc` 导出 |
| 🎁 每日畅听会员领取 (`v2.5.2`) | [echo-music-daily-vip-claim](https://github.com/xhd2005/echo-music-daily-vip-claim) | 原生 `Dialog` 畅听账本与四步打卡可视化进度（特权升级识别、听歌打卡四通道官方上报链告别 `ERR_EMPTY_RESPONSE`、真实失败诊断与单步「重试」）、当月打卡日历网格 + 多账号 SQLite 独立账本 |
| 📊 听歌统计 (`v1.5.0`) | [echo-music-stats](https://github.com/xhd2005/echo-music-stats) | 原生 `SliverHeader` + 吸顶筛选栏 + `DatePicker` + `RollingNumber` KPI；排行榜双击防误切歌、高光卡播放修复、点击 365 天热力图或 Top 歌手侧滑打开 `Drawer` 下钻流水（支持删单条挂机记录）及 `Dialog` 分账号安全清理 |

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
