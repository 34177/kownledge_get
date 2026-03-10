# AI 日报自动化工作流配置

**版本:** 1.0  
**创建时间:** 2026-03-10  
**最后更新:** 2026-03-10

---

## 工作流程概述

每日自动生成两份独立报告：
1. **技术新闻日报** (news/) - 行业动态、公司动态、投融资
2. **技术论文日报** (papers/) - arXiv 论文深度分析

---

## 每日执行清单

### 09:00 CST 自动执行

#### 步骤 1: 数据采集 (约 5-10 分钟)

**新闻源浏览:**
- [ ] WIRED AI - 获取最新 AI 行业新闻
- [ ] TechCrunch AI - 创业公司和投融资动态
- [ ] VentureBeat AI - 企业 AI 应用新闻
- [ ] MIT Technology Review - 深度技术分析
- [ ] OpenAI News - 官方公告
- [ ] Anthropic News - 官方公告
- [ ] Google AI Blog - 研究进展
- [ ] DeepMind Blog - 研究成果
- [ ] Meta AI - 研究进展

**论文源浏览:**
- [ ] arXiv cs.AI - 获取当日新增论文列表
- [ ] arXiv cs.LG - 机器学习论文
- [ ] arXiv cs.CL - 计算语言学论文
- [ ] arXiv cs.CV - 计算机视觉论文
- [ ] Hugging Face Papers - 热门论文

#### 步骤 2: 内容筛选 (约 3-5 分钟)

**新闻筛选标准:**
- 融资新闻：金额 > $100M
- 产品发布：主流 AI 公司重要产品
- 政策监管：政府级 AI 政策
- 行业趋势：有数据支撑的趋势分析
- 争议事件：AI 安全、伦理相关

**论文筛选标准:**
- 选择 3-5 篇重点论文深度分析
- 优先选择：
  - 知名机构 (顶尖大学、大厂研究院)
  - 热门方向 (智能体、多模态、大模型)
  - 实用价值 (基准测试、工具库)
  - 突破性进展 (SOTA、新方法)

#### 步骤 3: 内容生成 (约 5-10 分钟)

**新闻报告要求:**
- 字数：1500-2500 字
- 结构：要闻 → 行业趋势 → 投融资 → 政策
- 风格：简洁、客观、信息密度高
- Emoji：极少使用 (仅用于小标题)
- 链接：每条新闻包含来源链接

**论文报告要求:**
- 字数：4000-6000 字
- 结构：概览 → 3-5 篇深度分析 → 其他论文 → 趋势分析
- 深度分析包含：
  - 研究背景与动机 (100-200 字)
  - 核心方法与技术贡献 (200-400 字)
  - 实验设置与结果 (150-300 字)
  - 技术意义与应用价值 (100-200 字)
- 风格：技术细节丰富、结构化
- 链接：论文 PDF + 项目主页 + 代码库

#### 步骤 4: 质量检查 (约 2 分钟)

**检查清单:**
- [ ] 日期正确 (YYYY-MM-DD)
- [ ] 数据来源标注清晰
- [ ] 链接可访问
- [ ] 无重复内容
- [ ] 技术术语准确
- [ ] 数字和单位正确
- [ ] 格式统一 (标题、列表、表格)

#### 步骤 5: 提交推送 (约 1 分钟)

```bash
cd /home/admin/.openclaw/workspace/kownledge_get
git add .
git commit -m "📊 AI 日报 YYYY-MM-DD

- 技术新闻：[3-5 个关键词]
- 技术论文：[2-3 个关键词]
- 自动生成于 09:00 CST"
git push origin main
```

---

## 质量标准

### 新闻报告质量指标

| 指标 | 要求 |
|------|------|
| 时效性 | 24 小时内新闻 |
| 准确性 | 事实无错误，数字准确 |
| 完整性 | 重要新闻不遗漏 |
| 客观性 | 中立陈述，无主观臆断 |
| 可读性 | 结构清晰，逻辑连贯 |

### 论文报告质量指标

| 指标 | 要求 |
|------|------|
| 深度 | 重点论文分析≥500 字/篇 |
| 准确性 | 方法、实验、结论准确 |
| 洞察 | 有技术趋势分析 |
| 实用性 | 包含项目链接和代码 |
| 覆盖度 | 覆盖 3-5 个研究方向 |

---

## 工具配置

### 浏览器配置

```bash
# 浏览器状态检查
openclaw browser status

# 如未运行，启动浏览器
openclaw browser start
```

### Cron 配置

```bash
# 查看当前 cron
crontab -l

# 编辑 cron
crontab -e

# 添加任务 (每天 09:00)
0 9 * * * /home/admin/.openclaw/workspace/scripts/ai-daily-fetch.sh >> /tmp/ai-daily-fetch.log 2>&1
```

### 日志查看

```bash
# 查看最新日志
tail -50 /tmp/ai-daily-fetch.log

# 查看完整日志
cat /tmp/ai-daily-fetch.log

# 实时监控
tail -f /tmp/ai-daily-fetch.log
```

---

## 故障处理

### 常见问题

**1. 浏览器服务不可用**
```bash
# 检查浏览器状态
openclaw browser status

# 重启浏览器
openclaw browser restart

# 检查 Chrome 是否安装
which google-chrome
```

**2. 网站无法访问**
- 检查网络连接
- 尝试备用数据源
- 记录失败原因

**3. Git 推送失败**
```bash
# 检查 token 是否有效
curl -H "Authorization: token $GITHUB_TOKEN" https://api.github.com/user

# 重新配置 git
git config user.name "OpenClaw AI Bot"
git config user.email "openclaw@local"
```

**4. 报告生成失败**
- 检查脚本权限：`chmod +x scripts/ai-daily-fetch.sh`
- 检查目录权限：`ls -la`
- 查看错误日志：`cat /tmp/ai-daily-fetch.log`

---

## 持续改进

### 每周回顾 (建议周日执行)

1. **检查报告质量**
   - 阅读本周所有报告
   - 标记质量问题
   - 记录改进点

2. **更新数据源**
   - 添加新的优质来源
   - 移除低质量来源
   - 调整优先级

3. **优化流程**
   - 简化重复步骤
   - 自动化手动操作
   - 更新配置文档

### 每月回顾

1. **统计分析**
   - 报告数量统计
   - 热门主题分析
   - 用户反馈收集

2. **技术升级**
   - 评估新工具
   - 更新依赖
   - 性能优化

---

## 配置备份

### 关键文件

```bash
# 工作流配置
/home/admin/.openclaw/workspace/kownledge_get/WORKFLOW.md

# 自动化脚本
/home/admin/.openclaw/workspace/scripts/ai-daily-fetch.sh

# Cron 配置
crontab -l > ~/cron-backup.txt

# Git 配置
git config --list > ~/git-config-backup.txt
```

### 恢复流程

```bash
# 恢复 cron
crontab ~/cron-backup.txt

# 恢复脚本
cp ~/scripts/ai-daily-fetch.sh /home/admin/.openclaw/workspace/scripts/

# 恢复权限
chmod +x /home/admin/.openclaw/workspace/scripts/ai-daily-fetch.sh
```

---

## 联系与支持

**GitHub Issues:** https://github.com/34177/kownledge_get/issues

**日志位置:** /tmp/ai-daily-fetch.log

**仓库位置:** /home/admin/.openclaw/workspace/kownledge_get

---

*本工作流文档应定期更新，反映最新的配置和最佳实践*
