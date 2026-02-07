# notesctl skill for OpenClaw

**English** | [中文](#中文)

This repository contains the **notesctl** OpenClaw skill (source) for managing **Apple Notes** on macOS via deterministic scripts.

It was written as a replacement for OpenClaw's original Apple Notes skill: the original one can occasionally produce a note titled "New Notes" and is token-expensive. This skill keeps the system logic deterministic and uses the LLM only once to produce the final output.

## Contents

- `skill/notesctl/` — skill source (SKILL.md + scripts + README)

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

Dependencies: the same as OpenClaw’s built-in **apple-notes** skill (memo). If you already use that skill, you likely have it installed; otherwise OpenClaw will prompt you to install it when needed.

## Install / Use

1) Clone/download this repository.

2) Copy `skill/notesctl/` into your OpenClaw skills directory.

   Note: disable OpenClaw's built-in Apple Notes skill to avoid conflicts.

3) Use it by asking the agent to write/search/export Apple Notes.

---

## 中文

这个仓库包含 **notesctl** 的 OpenClaw skill（源码 + 源码），用于在 macOS 上通过确定性脚本管理 **Apple Notes（备忘录）**。

它是为了替代 OpenClaw 原有的 Apple Notes skill：原 skill 偶尔会生成标题为 "New Notes" 的笔记，而且非常费 token。这个版本把系统逻辑做成确定性的脚本流程，除了必要的输出生成外，只调用一次 LLM 然后输出。

### 内容

- `skill/notesctl/`：skill 源码（SKILL.md + scripts + README）

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

补充：依赖与 OpenClaw 自带的 **apple-notes** skill 相同（memo）。如果你已经用过自带 skill 通常已安装；否则在需要时 OpenClaw 会提示安装。

### 安装 / 使用

- 克隆/下载本仓库。

- 拷贝 `skill/notesctl/` 到OpenClaw skills目录.

- 注意: 要停用自带的Apple Notes skill 避免冲突.

- 直接对 agent 说你要写/搜/导出 Notes 即可。
