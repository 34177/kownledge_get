# API 技术文档采集系统

自动采集各大技术平台的 API 文档，支持 Git 仓库、动态网站、API 接口三种采集方式。

## 🎯 功能特性

- **Git 仓库采集** - 克隆并提取 GitHub/GitLab 上的技术文档
- **动态网站采集** - 使用浏览器自动化抓取 JS 渲染的文档网站
- **API 接口采集** - 直接调用 REST API 获取结构化数据
- **定时执行** - 每日自动更新，Git 自动提交推送
- **统一索引** - 自动生成文档索引和摘要

## 📁 目录结构

```
kownledge_get/
├── docs/                    # 采集的文档输出
│   ├── react-docs.md
│   ├── typescript-handbook.md
│   ├── mdn-javascript.md
│   ├── openai-api.md
│   ├── anthropic-api.md
│   └── INDEX.md            # 文档索引
├── sources.json            # 采集源配置
├── README.md
└── WORKFLOW.md             # 工作流程说明
```

## 🔧 配置采集源

编辑 `sources.json` 添加你的文档源：

### Git 仓库
```json
{
  "git": [{
    "name": "React 文档",
    "url": "https://github.com/facebook/react.git",
    "branch": "main",
    "paths": ["packages/react.dev/content"],
    "output": "react-docs.md",
    "enabled": true
  }]
}
```

### 动态网站
```json
{
  "browser": [{
    "name": "OpenAI API 文档",
    "url": "https://platform.openai.com/docs",
    "selector": "main",
    "output": "openai-api.md",
    "enabled": true,
    "refresh": "daily"
  }]
}
```

### API 接口
```json
{
  "api": [{
    "name": "GitHub Releases",
    "endpoint": "https://api.github.com/repos/facebook/react/releases",
    "auth": false,
    "output": "github-releases.json",
    "enabled": true
  }]
}
```

## 🚀 使用方式

### 手动执行
```bash
/home/admin/.openclaw/workspace/scripts/api-docs-fetch.sh
```

### 定时任务 (Cron)
```bash
# 每天 09:00 执行
crontab -e
# 添加：
0 9 * * * /home/admin/.openclaw/workspace/scripts/api-docs-fetch.sh >> /tmp/api-docs-fetch.log 2>&1
```

### 查看日志
```bash
tail -f /tmp/api-docs-fetch.log
```

## 📊 支持的文档源

| 类型 | 示例 | 更新频率 |
|------|------|----------|
| Git | React, Vue, TypeScript, Rust | 每日 |
| Browser | MDN, OpenAI, Anthropic, Hugging Face | 每日/每周 |
| API | GitHub Releases, HF Blog | 每日 |

## 🔐 认证配置

对于需要认证的 API，在 `sources.json` 中设置 `"auth": true`，然后在脚本中配置环境变量：

```bash
export GITHUB_TOKEN="your_token"
export HUGGINGFACE_TOKEN="your_token"
```

## 📝 许可证

MIT
