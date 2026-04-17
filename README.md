# Chian's Claude Code Skills

Chian 的 Claude Code skill 统一管理仓库,供个人使用。

## 分层架构

| 目录 | 加载方式 | 用途 |
|---|---|---|
| `core/` | 软链到 `~/.claude/skills/`,全局常驻 | 日常高频(每日复盘) |
| `research/` | 软链到 BioAdhesion 项目,仅该项目可见 | 学术研究(文献检索等) |
| `content-creation/` | 按需拖拽 | 内容生产(小红书、视频 pipeline 等) |
| `perspective/` | 按需拖拽 | 女娲蒸馏的视角 skill(芒格、Naval、段永平) |
| `meta/` | 女娲可软链常驻 | 造 skill 的 skill |
| `archived/` | 不软链 | 存档备用 |

## 安装

```bash
git clone git@github.com:Really-well/chian-claude-skills.git ~/claude-skills-repo
cd ~/claude-skills-repo
git submodule update --init --recursive
```

### 软链到用户级(全局常驻)

```bash
mkdir -p ~/.claude/skills
ln -sfn ~/claude-skills-repo/core/daily-review ~/.claude/skills/daily-review
ln -sfn ~/claude-skills-repo/meta/nuwa-skill ~/.claude/skills/nuwa-skill
```

### 软链到项目级

```bash
mkdir -p <你的项目>/.claude/skills
ln -sfn ~/claude-skills-repo/research/literature-search <你的项目>/.claude/skills/literature-search
```

## 跨端同步

本地 Mac 改 → `git push` → 腾讯云 OpenClaw `git pull` → 三端一致。

## License

MIT © Really-well (Chian)