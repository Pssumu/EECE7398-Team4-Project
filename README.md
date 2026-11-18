# EECE7398-Team4-Project

EECE7398 Team 4 期末项目的公共仓库，用来存放项目计划、参考资料和每个成员的工作文件。
Shared repository for the EECE7398 Team 4 final project: plans, references, and each member's work.

## 目录结构 / Layout

```
.
├── plans-and-ideas/      项目计划与想法：proposal、review、会议记录、项目指导
├── references/           参考资料：论文等
└── members/              成员个人文件夹
    ├── Pssumu/
    ├── alemarefanim/
    ├── Jan-Zhao11/
    └── Yeyaohui11/
```

## 协作规则 / Rules

1. **个人文件夹只归本人。** 每位成员只能在 `members/<自己的 GitHub 用户名>/` 里添加、修改、删除文件。
   **Your folder is yours alone.** Only add, edit or delete files under `members/<your GitHub username>/`.
2. **别人的文件夹只读。** 可以查看、下载其他成员的文件；需要改动时，复制到自己的文件夹里再改，或者联系文件夹的主人。
   **Other members' folders are read-only.** View and download freely; to build on someone's file, copy it into your own folder or ask its owner.
3. **公共文件夹由仓库管理员 Pssumu 维护。** `plans-and-ideas/`、`references/` 和根目录文件（README、AGENTS.md 等）的改动请先在群里说一声，或者把新版本放进自己的文件夹，由 Pssumu 整理进来。
   **Shared folders are maintained by the repo owner (Pssumu).** For changes to `plans-and-ideas/`, `references/` or root files, coordinate first or drop the new version in your own folder.
4. **`main` 分支禁止强制推送和删除。** 推送前先 `git pull`。
   **No force pushes or deleting `main`.** Always `git pull` before you push.
5. **提交信息写清楚改了什么。** 每次提交都有记录，越界的改动会被发现并撤回。
   **Write clear commit messages.** All changes are logged; edits outside your folder will be reverted.

## 日常操作 / Everyday workflow

```bash
git clone https://github.com/Pssumu/EECE7398-Team4-Project.git   # 第一次 / first time
git pull                                                         # 开始工作前 / before working
git add members/<你的用户名>/
git commit -m "说明改了什么 / what changed"
git push
```

> Word、PDF 这类二进制文件 git 没法合并。同一个文件请不要两人同时改。
> Binary files (Word, PDF) can't be merged by git — don't edit the same file at the same time.
> 单个文件请小于 50MB，GitHub 拒收超过 100MB 的文件。 Keep files under 50 MB; GitHub rejects files over 100 MB.

## AI agent

使用 AI 编程助手（Claude Code、Codex、Cursor 等）操作本仓库前，必须先阅读 [AGENTS.md](AGENTS.md) 并遵守其中的规则。
Any AI agent working in this repository must read and follow [AGENTS.md](AGENTS.md) first.
