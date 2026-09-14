---
name: doc-sync
description: 该技能会将 my_learningdita 分支上更新的 DITA 教程文件自动同步到网站。当用户要求「同步 DITA 教程」「同步 my_learningdita 的更新」「把新课程发布到网站」时使用。
---

# 同步 DITA 教程

## 同步正文

调用 `dita-doc-sync` 子智能体，由它完成：

1. 获取更新文件列表
2. 格式转换
3. 更新导航目录

调用前询问：“是否需要指定目标路径（target_path）和导航目录的一级标题（heading1）? 如果需要，请输入；如果不需要，请输入`否`或`N`”。如果用户指定了目标路径和一级标题，请将其传给子智能体。

## 生成参考答案页

如果更新的文件中包含随堂练习和课后练习，执行 `/create-possible-answers` 命令。

执行前询问：“随堂练习和课后练习的参考答案（snippet_folder）在哪里?” 

执行完成后，更新导航目录（`mkdocs.yml` 中的 `nav`）。