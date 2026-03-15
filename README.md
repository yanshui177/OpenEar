# OpenEar 🤖

**你的私人 AI 情报助手**

---

## 📖 项目介绍

OpenEar 是一个自动化的 AI 新闻收集与推送系统，每天定时从 20 个优质来源抓取最新 AI 领域动态，推送到你的钉钉/企业微信，并生成详细的 Markdown 文档存档。

---

## 🎯 核心功能

### ✅ 每日推送

- **时间：** 每天早上 09:30（Asia/Shanghai）
- **渠道：** 钉钉 + 企业微信
- **内容：** 24 小时内最新 AI 新闻
- **格式：** 简洁版推送 + 详细版文档

### 📰 新闻来源（65 个）

**AI 动态（20 个）**
- 官方：OpenAI, Anthropic, Google AI, Meta AI, 通义千问，智谱 AI, Hugging Face, Stability AI
- 媒体：机器之心，量子位，AI 科技评论，新智元，TechCrunch AI
- 社区：知乎 AI 话题，Reddit r/MachineLearning, arXiv CS.AI, Papers With Code
- 工具：GitHub Trending AI, LangChain Blog, MIT Tech Review AI

**AI 论文（20 个）**
- arXiv：CS.AI, CS.LG, CS.CL, CS.CV, CS.NE
- 平台：Papers With Code (Latest, SOTA)
- 实验室：OpenAI Research, Google AI, Meta AI, DeepMind, Stanford HAI, MIT CSAIL, Berkeley BAIR
- 会议/期刊：NeurIPS, ICML, ICLR, CVPR, ACL, Nature Machine Intelligence

**AI Infra & MLSys（25 个）**
- arXiv：CS.DC, CS.PF, CS.AR, ML Systems
- 会议：MLSys, EuroMLSys, SOSP, OSDI, ATC, SC
- 框架：PyTorch, TensorFlow, JAX, Hugging Face, vLLM, Ray, NVIDIA
- 芯片：NVIDIA Research, Google TPU, Cerebras, Groq, SambaNova

### 📁 文档存档

- **位置：** `/AI/Daily/YYYY-MM-DD.md`
- **格式：** Markdown 详细版
- **内容：** 每条新闻 100-1000 字深度分析
- **同步：** 自动推送到 GitHub

---

## 🚀 使用方式

### 查看今日新闻

1. **钉钉/企业微信** - 每天早上 9:30 自动推送
2. **GitHub** - 访问 [AI/Daily](https://github.com/yanshui177/OpenEar/tree/main/AI/Daily) 目录
3. **本地** - `/root/nas/docs/vivi/OpenEar/AI/Daily/`

### 新闻分级

| 类别 | 级别 | 字数 | 说明 |
|------|------|------|------|
| AI 动态 | 重磅新闻 | 500-1000 字 | 深度分析、技术细节、行业影响 |
| AI 动态 | 重要新闻 | 200-500 字 | 核心亮点、技术细节、影响分析 |
| AI 动态 | 一般新闻 | 100-200 字 | 简要介绍、关键信息 |
| 论文精选 | 所有论文 | 200-500 字 | 标题、机构、核心贡献、技术亮点、应用前景 |
| AI Infra | 所有技术 | 200-500 字 | 技术细节、性能提升、应用场景 |

---

## ⚙️ 技术架构

```
┌─────────────┐
│ Cron 定时   │ 每天 09:30 触发
│ 09:30       │
└──────┬──────┘
       │
       ↓
┌─────────────┐
│ 新闻抓取器   │ 65 个来源 web_fetch
│             │ (AI 动态 + 论文 + AI Infra)
└──────┬──────┘
       │
       ↓
┌─────────────┐
│ AI 总结生成器 │ 分类 + 摘要 + 分析
└──────┬──────┘
       │
       ├──────────┬──────────┐
       ↓          ↓          ↓
  ┌────────┐ ┌────────┐ ┌────────┐
  │ 钉钉   │ │ 企业微信│ │ GitHub │
  │ 推送   │ │ 推送   │ │ 存档   │
  └────────┘ └────────┘ └────────┘
```

---

## 📂 目录结构

```
OpenEar/
├── README.md              # 本文件
├── AI/
│   └── Daily/             # 每日新闻存档
│       ├── 2026-03-13.md
│       ├── 2026-03-14.md
│       └── ...
└── ...
```

---



## 📊 新闻筛选标准

### 时间要求

- **AI 动态：** 24 小时内（不足可扩展到 48 小时）
- **AI 论文：** 7 天内新论文
- **AI Infra/MLSys：** 7 天内更新

### 重大新闻即时推送

满足以下之一立即推送（不等待 9:30）：
- 大模型新版本发布（GPT-5, Claude 5 等）
- 融资金额 ≥ 1 亿美元
- 国家级 AI 政策/法规发布
- 重大安全事件

---

## 🛠️ 部署环境

| 组件 | 版本 |
|------|------|
| 操作系统 | Alibaba Cloud Linux 3.2104 |
| OpenClaw | 2026.3.11 |
| Node.js | v22.22.1 |
| Git | 2.43.7 |

---

## 📝 更新日志

### 2026-03-13
- ✅ 项目初始化
- ✅ 配置 20 个新闻来源
- ✅ 设置每天 9:30 定时推送
- ✅ 钉钉推送测试成功
- ✅ GitHub 自动存档

---

## 🤝 贡献

本项目为个人使用，暂不接受外部贡献。

---

## 📄 许可证

MIT License

---

## 👤 作者

**OpenEar** - 你的私人 AI 情报助手

由 **OpenClaw** 驱动，运行在阿里云 ECS。

---

<div align="center">

**📬 每天 9:30，AI 动态一网打尽！**

Made with ❤️ by OpenEar

</div>
