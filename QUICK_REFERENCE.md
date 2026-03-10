# AI 日报系统 - 快速参考

## 核心配置

**执行时间:** 每天 09:00 CST  
**脚本:** `/home/admin/.openclaw/workspace/scripts/ai-daily-fetch.sh`  
**日志:** `tail -20 /tmp/ai-daily-fetch.log`

## 报告位置

- **新闻:** `kownledge_get/news/ai-news-YYYY-MM-DD.md`
- **论文:** `kownledge_get/papers/ai-papers-YYYY-MM-DD.md`

## 质量标准

| 报告 | 字数 | 内容 |
|------|------|------|
| 新闻 | 1.5K-2.5K | 行业动态、公司、投融资 |
| 论文 | 4K-6K | 3-5 篇深度分析 |

## 常用命令

```bash
# 手动执行
/home/admin/.openclaw/workspace/scripts/ai-daily-fetch.sh

# 查看 cron
crontab -l

# 检查浏览器
openclaw browser status

# 查看 git 状态
cd kownledge_get && git status
```

## 数据源

**新闻 (9):** WIRED, TechCrunch, VentureBeat, MIT TR, OpenAI, Anthropic, Google, DeepMind, Meta

**论文 (5):** arXiv cs.AI/LG/CL/CV, Hugging Face

## 故障处理

1. 浏览器问题 → `openclaw browser restart`
2. Git 推送失败 → 检查网络和 token
3. 报告未生成 → 查看日志 `/tmp/ai-daily-fetch.log`

## 文档

- **WORKFLOW.md** - 详细工作流程
- **README.md** - 项目说明
- **SETUP_SUMMARY.md** - 配置总结
