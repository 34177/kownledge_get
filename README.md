# AI 前沿日报自动采集系统

全自动的 AI 前沿信息采集系统，由 OpenClaw 驱动，每日生成两份独立报告。

---

## 报告结构

本项目生成两种独立报告：

### 1. 技术新闻日报 (news/)

**定位:** 行业动态、公司动态、投融资、政策法规

**内容:**
- 公司动态 (OpenAI, Anthropic, Google, Meta 等)
- 投融资新闻
- 政策法规与监管
- 行业趋势分析
- 产品发布与合作

**数据来源:**
- WIRED AI
- TechCrunch AI
- VentureBeat AI
- MIT Technology Review
- 公司官方博客

**文件名:** `news/ai-news-YYYY-MM-DD.md`

---

### 2. 技术论文日报 (papers/)

**定位:** 学术论文深度解读、技术分析

**内容:**
- arXiv 当日新增论文概览
- 3-5 篇重点论文深度分析
  - 研究背景与动机
  - 核心方法与技术贡献
  - 实验设置与结果
  - 技术意义与应用价值
- 其他值得关注论文列表
- 技术趋势分析

**数据来源:**
- arXiv cs.AI, cs.LG, cs.CL, cs.CV
- Hugging Face Papers
- Papers With Code

**文件名:** `papers/ai-papers-YYYY-MM-DD.md`

---

## 目录结构

```
kownledge_get/
├── README.md
├── news/                    # 技术新闻报告
│   ├── ai-news-2026-03-08.md
│   ├── ai-news-2026-03-09.md
│   └── ai-news-2026-03-10.md
├── papers/                  # 技术论文报告
│   ├── ai-papers-2026-03-08.md
│   ├── ai-papers-2026-03-09.md
│   └── ai-papers-2026-03-10.md
└── scripts/
    └── ai-daily-fetch.sh    # 自动采集脚本
```

---

## 报告特点

### 新闻报告
- 简洁明了，重点突出
- 纯文字为主，少用图表
- 按主题分类 (公司、行业、政策)
- 包含来源链接

### 论文报告
- 深度分析 3-5 篇重点论文
- 结构化呈现 (背景、方法、实验、意义)
- 技术细节丰富
- 包含论文链接和项目主页

---

## 自动化配置

### 执行时间

每天 09:00 (CST) 自动执行

### Cron 配置

```bash
0 9 * * * /home/admin/.openclaw/workspace/scripts/ai-daily-fetch.sh
```

### 查看执行日志

```bash
cat /tmp/ai-daily-fetch.log
```

### 手动触发

```bash
/home/admin/.openclaw/workspace/scripts/ai-daily-fetch.sh
```

---

## 技术栈

- **执行环境:** OpenClaw (Linux)
- **浏览器:** Chrome + OpenClaw Browser
- **抓取工具:** browser, web_fetch, pdf
- **脚本:** Bash + Git
- **调度:** cron
- **存储:** GitHub Repository

---

## 浏览与学习能力

系统具备完整的自主浏览和学习能力：

### 网页浏览
- 打开任意网页
- 点击导航
- 表单填写
- 页面快照
- 内容提取
- 多标签页管理

### 论文学习
- 读取 arXiv HTML 版本
- 提取摘要、方法、实验、结论
- 跨论文对比分析
- 技术要点总结

### 内容生成
- 自主分析总结
- 结构化报告生成
- 技术趋势洞察

---

## 查看最新报告

### 新闻报告
https://github.com/34177/kownledge_get/tree/main/news

### 论文报告
https://github.com/34177/kownledge_get/tree/main/papers

---

## 订阅更新

点击仓库右上角的 **Watch** 按钮，每次新报告推送时会收到通知。

---

## 数据源列表

### 新闻媒体
| 网站 | URL |
|------|-----|
| WIRED AI | https://www.wired.com/tag/artificial-intelligence/ |
| TechCrunch AI | https://techcrunch.com/category/artificial-intelligence/ |
| VentureBeat AI | https://venturebeat.com/category/ai/ |
| MIT Tech Review | https://www.technologyreview.com/topic/artificial-intelligence/ |

### 研究机构
| 网站 | URL |
|------|-----|
| arXiv cs.AI | https://arxiv.org/list/cs.AI/recent |
| arXiv cs.LG | https://arxiv.org/list/cs.LG/recent |
| Hugging Face Papers | https://huggingface.co/papers |
| Papers With Code | https://paperswithcode.com |

### 公司博客
| 公司 | URL |
|------|-----|
| OpenAI News | https://openai.com/news/ |
| Anthropic News | https://www.anthropic.com/news |
| Google AI | https://ai.google/ |
| DeepMind Blog | https://deepmind.google/discover/blog/ |
| Meta AI | https://ai.meta.com/ |

---

## 反馈与建议

如需调整：
- 增加新的数据源
- 修改报告格式
- 调整执行时间
- 增加特定主题分析

请通过 GitHub Issues 提出。

---

*最后更新：2026-03-10*  
*维护者：OpenClaw 自动采集系统*  
*GitHub: https://github.com/34177/kownledge_get*
