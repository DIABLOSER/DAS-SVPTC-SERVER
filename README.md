<div align="center">
  <img src="https://github.com/DIABLOSER/DAS-SVPTC/blob/main/src/assets/img/logo.png" alt="logo" width="200" height="200" />
</div>

# 📦 短视频文本评论动态分析系统服务端

> 基于哔哩哔哩开放 API 的短视频评论情感与行为数据可视化平台

本项目致力于构建一个面向 **Bilibili 短视频平台** 的评论数据动态分析系统，采用 **前后端分离架构**，实现对用户评论内容的实时采集、智能分析与交互式可视化展示，帮助用户更全面地洞察观众反馈、舆情变化及潜在热点内容。

项目涵盖从登录认证、视频内容获取到评论文本深度挖掘与图形展示的完整数据流程，适用于数据分析、自然语言处理、用户研究等多个场景。

服务端基于 Python 的 Flask 框架开发，主要负责处理前端请求、调用 Bilibili 接口、分析评论数据，并将可视化图表和分析结果返回前端展示。

---

## 🚀 功能模块

### 1. 用户扫码登录（基于 Bilibili 二维码）

- 获取登录二维码：`/api/qrcode`
- 轮询二维码状态：`/api/qrcode/polling`
- 获取用户登录凭证：返回 `SESSDATA`、`DedeUserID`

> ✅ 使用模拟浏览器行为完成扫码登录，无需用户输入账号密码，兼顾安全性与用户便利性。

---

### 2. 用户信息与投稿数据

- 获取用户基本信息（昵称、头像、粉丝数等）
- 获取用户投稿视频列表（支持分页）
- 获取单个视频详情信息（播放地址、时长、点赞数、评论数等）

---

### 3. 评论数据获取与分析

- 分页获取评论列表
- 评论数据多维分析：
  - 情感分析（正面 / 中性 / 负面）
  - 评论词频统计
  - 用户性别与地区分布
  - 评论发布时间趋势分析
  - KMeans 文本聚类分析

---

### 4. 可视化图表生成

以下图表均自动生成并保存在 `output/` 目录中，前端可通过静态资源方式访问：

- 词云图（评论关键词）
- 性别分布图（饼状图）
- 评论时间趋势图（折线图）
- 情感极性分析柱状图
- 用户地区分布图
- 聚类结果散点图（基于文本相似度）

---

### 5. 代理服务

- 图片代理：用于解决跨域问题，支持直接展示 B 站图片
- 视频代理：支持视频流式传输，绕过防盗链限制

---

### 6. 文件与日志管理

- 所有评论分析结果保存为 `.csv` 文件，便于本地下载与二次研究
- 支持运行日志、请求日志与错误日志记录，方便调试与维护

---

## ⚠️ 免责声明

本项目仅供 **学术研究与学习使用**，所有数据均来自哔哩哔哩官方公开 API，不涉及任何商业用途或隐私数据抓取。如有侵权或违反平台规定，请及时联系作者处理。

---

## 📬 联系作者

如有建议或合作意向，欢迎通过以下方式与我联系：

- 📧 Email：`daboluo719@gmail.com`
- 🔗 项目地址：[GitHub - DAS-SVPTC](https://github.com/DIABLOSER/DAS-SVPTC)

---

> 如果你喜欢这个项目，欢迎 ⭐Star 和 🍴Fork！你的支持是我持续优化的最大动力！

