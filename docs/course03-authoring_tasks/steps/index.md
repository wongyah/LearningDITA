# 插入操作流程

## 学习目标

- 了解 `<steps>` 元素在 `<taskbody>` 元素中的位置
- 了解操作流程的核心元素以及它们的用途
- 学会区分 `<choices>` 和 `<choicetable>` 元素
- 学会创建子步骤，并且明白子步骤与步骤之间的区别

## 学习时长

大约 1 小时。

## 课程简介

在 `<steps>` 元素（请注意，元素名称是复数）中，可以插入 `<step>` 元素（请注意，元素名称是单数）。`<step>` 元素可以用来编写单个步骤的操作说明。

将任务型主题发布之后，操作流程通常以有序列表（即数字列表）的格式显示。每个操作步骤的标签（比如数字编号和一些标点符号、词语“第#步”）取决于发布设置（也就是样式表）。编写操作步骤时，大多数DITA编辑器都会在每个步骤的旁边显示相应的数字编号。

!!! note "注意"
    本讲的主要内容是这些元素的基本用法。如果你想了解每个元素的详细用法，请参见《OASIS DITA 1.3 规范》中的 [任务型主题](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/containers/task-elements.html#task2)一节。

## 相关资料

- [《DITA写作指南》：操作流程中的语义](https://www.oxygenxml.com/dita/styleguide/Syntax_and_Markup/c_Semantics_in_Steps.html)
- [《DITA写作指南》：指令元素](https://www.oxygenxml.com/dita/styleguide/Syntax_and_Markup/c_The_command_Element.html)
- [《DITA写作指南》：必选步骤和可选步骤](https://www.oxygenxml.com/dita/styleguide/Syntax_and_Markup/c_Required_and_Optional_Steps.html)
- [《DITA写作指南》：选项表](https://www.oxygenxml.com/dita/styleguide/Syntax_and_Markup/c_Choice_Tables.html)
- [《DITA写作指南》：操作步骤中的子步骤](https://www.oxygenxml.com/dita/styleguide/Syntax_and_Markup/c_Sub_Steps.html)
- [《DITA写作指南》：操作步骤中的安全信息和额外信息](https://www.oxygenxml.com/dita/styleguide/Syntax_and_Markup/c_Notes_in_Steps.html)