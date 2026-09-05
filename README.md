# 微信账号文章库

本仓库采用参考仓库的展示方式：大量独立 Markdown 文章直接平铺在仓库根目录。

- 文章数量：600 篇
- 文件格式：Markdown
- 文件名保留 `【关键词】` 占位符，方便后续批量替换
- 每篇正文顶部包含：`TG:qszxc686`
- 关键词配置：`keywords.txt`
- 生成脚本：`tools/generate_articles.py`

> 文章主题以微信账号安全、注册、登录、隐私、设备管理、异常处理等合规内容为主。

## 批量关键词

把 100 个关键词逐行放进 `keywords.txt`。生成脚本会按顺序循环使用关键词：第 1、101、201、301、401、501 篇使用第 1 个关键词，以此类推。

运行：

```bash
python tools/generate_articles.py
```

默认生成 600 篇，文件名保留 `【关键词】`。如需把关键词实际写入文件名：

```bash
python tools/generate_articles.py --replace-placeholder
```
