---
name: doc-sync
description: 该技能会将 my_learningdita 分支上更新的 DITA 教程文件自动同步到网站。
---

# 同步 DITA 教程


## 获取更新文件列表

```git
git diff --name-only my_learningdita~1 my_learningdita -- "*.dita"
```

## 格式转换

如果是课程简介（文件中包含 `<lcObjectives>` 元素），执行 `\dita2md-index` 命令。否则，执行 `\dita2md` 命令。

## 更新导航目录

`\update-nav`