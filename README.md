<div align="center">

# 🔌 xhd2005 的 EchoMusic 插件源

**一个源，收录全部插件 —— 每日畅听会员领取 + 听歌统计**

[![EchoMusic](https://img.shields.io/badge/EchoMusic-%E2%89%A52.2.7--beta.9-31cfa1?style=flat-square&logo=electron&logoColor=fff)](https://github.com/hoowhoami/EchoMusic)

</div>

这是 [EchoMusic](https://github.com/hoowhoami/EchoMusic) 插件市场的**聚合插件源**。添加本仓库地址后，即可同时发现并安装下列插件，无需逐个添加源。

## 🚀 快速开始

在 EchoMusic → 设置 → 插件管理 → 插件市场 → **添加源**：

```text
https://github.com/xhd2005/echo-music-plugins
```

## 📦 收录插件

| 插件 | 仓库 | 说明 |
| --- | --- | --- |
| 🎁 每日畅听会员领取 | [echo-music-daily-vip-claim](https://github.com/xhd2005/echo-music-daily-vip-claim) | 每日领取 1 天畅听会员，支持自动领取与当月记录 |
| 📊 听歌统计 | [echo-music-stats](https://github.com/xhd2005/echo-music-stats) | 本地听歌统计报告，数据 100% 保存在本机 |

## 🔧 工作原理

本仓库根目录的 [`echo-plugins.json`](echo-plugins.json) 是插件源索引，通过每条插件的 `repo` 字段指向其独立仓库：

```json
{
  "name": "xhd2005 的 EchoMusic 插件源",
  "plugins": [
    { "id": "daily-vip-claim", "repo": "xhd2005/echo-music-daily-vip-claim", "tags": ["vip", "会员", "畅听", "每日领取"] },
    { "id": "music-stats",     "repo": "xhd2005/echo-music-stats",     "tags": ["统计", "报告", "可视化", "本地"] }
  ]
}
```

- 各插件独立仓库、独立版本、独立 release，互不影响
- 新增 / 更名插件时，仅需更新本仓库的索引一行

## 📄 许可证

各插件遵循其各自仓库的许可证（GPL-3.0）。
