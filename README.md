# notesctl skill for OpenClaw

**English** | [中文](#中文)

This repository contains the **notesctl** OpenClaw skill (source + packaged `.skill` file) for managing **Apple Notes** on macOS via deterministic scripts.

It was written as a replacement for OpenClaw's original Apple Notes skill: the original one can occasionally produce a note titled "New Notes" and is token-expensive. This skill keeps the system logic deterministic and uses the LLM only once to produce the final output.

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

它是为了替代 OpenClaw 原有的 Apple Notes skill：原 skill 偶尔会生成标题为 "New Notes" 的笔记，而且非常费 token。这个版本把系统逻辑做成确定性的脚本流程，除了必要的输出生成外，只调用一次 LLM 然后输出。

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
