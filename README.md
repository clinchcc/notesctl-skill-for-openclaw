# notesctl skill for OpenClaw

**English** | [中文](#中文)

This repository contains the **notesctl** OpenClaw skill (source + packaged `.skill` file) for managing **Apple Notes** on macOS via deterministic scripts.

## Contents

- `skill/notesctl/` — skill source (SKILL.md + scripts + README)
- `notesctl.skill` — packaged skill file for import/sharing

## What it can do

- Create a new note (title/body/folder)
- Create a new note via JSON stdin (stable automation)
- List notes in a folder
- Search notes (optionally scoped to a folder)
- Export a matched note (interactive selection)

## Requirements

- macOS
- `python3`, `osascript`
- `memo` CLI (used by the scripts)

## Install / Use

1) Download `notesctl.skill` from **Releases**.

2) Import/install the skill in your OpenClaw setup.

3) Use it by asking the agent to write/search/export Apple Notes.

---

## 中文

这个仓库包含 **notesctl** 的 OpenClaw skill（源码 + 打包好的 `.skill` 文件），用于在 macOS 上通过确定性脚本管理 **Apple Notes（备忘录）**。

### 内容

- `skill/notesctl/`：skill 源码（SKILL.md + scripts + README）
- `notesctl.skill`：打包好的 skill 文件，可直接导入/分享

### 功能

- 新建备忘录（标题/正文/文件夹）
- 通过 JSON stdin 新建备忘录（更稳定，适合自动化）
- 列出某个文件夹下的备忘录
- 搜索备忘录（可限定文件夹）
- 导出匹配的备忘录（交互式选择）

### 依赖

- macOS
- `python3`, `osascript`
- `memo` 命令行工具（脚本依赖）

### 安装 / 使用

1）从 **Releases** 下载 `notesctl.skill`。

2）在你的 OpenClaw 环境中导入/安装该 skill。

3）直接对 agent 说你要写/搜/导出 Notes 即可。
