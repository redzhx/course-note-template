# Course Note Template

Claude Code 课程笔记处理工作流模板。配合 [image-ocr](https://github.com/redzhx/claude-skills) 和 [notes-supplement](https://github.com/redzhx/claude-skills) 两个 skill，将原始课程笔记（含图片和语音文稿）自动整理为出版级 Markdown。

## 工作流

```
原始笔记 (含图片)  ──→  image-ocr  ──→  OCR 整合版 (_ocr.md)
原始笔记 (含STT文稿) ──→  notes-supplement ──→  出版级 Markdown (_出版级.md)
```

两步可独立使用，无图片时可跳过第一步。

## 使用方法

```bash
# 1. 拉取 skills 并安装到用户级（仅首次）
git clone git@github.com:redzhx/claude-skills.git ~/claude-skills
ln -s ~/claude-skills/*/ ~/.claude/skills/

# 2. 克隆本模板创建课程目录
git clone git@github.com:redzhx/course-note-template.git 课程目录
cd 课程目录

# 3. 编辑 CLAUDE.md，修改标题和目录结构

# 4. 将笔记文件复制到目录中

# 5. 在 Claude Code 中打开此目录开始处理
```

## 文件结构

```
.
├── CLAUDE.md                        # 项目说明 + AI 工作流指令（按需修改）
└── .claude/
    └── settings.local.json          # 权限配置（允许读写执行等操作）
```

## 前置条件

- Claude Code (CLI 或桌面版)
- 已安装 `image-ocr`、`notes-supplement` skill（使用上方安装命令）

## 相关仓库

- [redzhx/claude-skills](https://github.com/redzhx/claude-skills) — 自定义 skill 集合

## License

MIT
