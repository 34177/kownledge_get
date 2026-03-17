# 计算机专业书籍库

自动采集和整理计算机专业领域的经典书籍（PDF 格式）。

## 📚 收录范围

- **计算机科学基础** - 算法、数据结构、计算机组成原理
- **编程语言** - Python, Java, C/C++, JavaScript, Go, Rust 等
- **人工智能** - 机器学习、深度学习、自然语言处理
- **软件工程** - 设计模式、架构、测试、DevOps
- **数据库** - SQL, NoSQL, 分布式系统
- **网络与安全** - 计算机网络、网络安全、密码学
- **系统编程** - 操作系统、Linux、编译原理

## 📁 目录结构

```
kownledge_get/
├── books/                    # PDF 书籍存储
│   ├── algorithms/          # 算法类
│   ├── programming/         # 编程语言类
│   ├── ai-ml/              # 人工智能类
│   ├── software-engineering/ # 软件工程类
│   ├── database/           # 数据库类
│   ├── network/            # 网络类
│   └── system/             # 系统类
├── sources.json            # 书籍源配置
├── INDEX.md                # 书籍索引
└── README.md
```

## 🔄 自动采集

每日自动从以下来源采集新书：

- GitHub 开源书籍仓库
- 开放获取教材网站
- 公共领域书籍库
- 高校开放课程资源

## 📖 使用方式

```bash
# 手动触发采集
/home/admin/.openclaw/workspace/scripts/cs-books-fetch.sh

# 查看日志
tail -f /tmp/cs-books-fetch.log
```

## 📋 书籍索引

详见 [INDEX.md](./INDEX.md)

## ⚠️ 版权说明

本仓库仅收录：
- 开放获取 (Open Access) 书籍
- 公共领域 (Public Domain) 书籍
- Creative Commons 许可书籍
- 作者明确允许分发的书籍

## 🤝 贡献

欢迎提交书籍推荐或资源链接。

## 📄 许可证

各书籍遵循其原有许可证
