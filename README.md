# GitHub Trending 每日归档

> 每日 GitHub 热门仓库榜单归档，fork 自 [bonfy/github-trending](https://github.com/bonfy/github-trending)。

## 📱 在线浏览

手机 / 网页版：[offddo.github.io/github-trending](https://offddo.github.io/github-trending/)

- 支持按日期浏览（2015 年至今）
- 支持按仓库名 / 描述搜索

## 数据

- 每日抓取 **Python / Swift / JavaScript / Go** 四个语言的热门仓库
- 数据由原作者 [bonfy](https://github.com/bonfy) 每日自动抓取并提交
- 本仓库通过 GitHub Actions 每日 **UTC 04:17（北京时间 12:17）** 自动从上游同步

## 自动同步

[.github/workflows/sync-upstream.yml](.github/workflows/sync-upstream.yml) 每天在 GitHub 云端自动执行：

```text
git fetch upstream → git rebase → git push --force
```

全程无需本地电脑参与。

## 目录结构

```text
.
├── 2026-*.md       # 2026 年数据（根目录）
├── 2025/ 2024/ …   # 更早年份数据
├── index.html      # 网页版查看器
└── scraper.py      # 原作者使用的抓取脚本
```

## 本地同步（可选）

本仓库采用 force push 同步，本地更新请执行：

```bash
git fetch origin master && git reset --hard origin/master
```

## License

MIT
