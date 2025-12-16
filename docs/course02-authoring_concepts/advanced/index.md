# 高级元素

## 学习目标

- 学习一些高级元素，以及如何在概念性主题中使用高级元素的最佳实践。
- 在概念型主题中，插入 `<codeblock>`、`<codeph>`、`<lq>`、`<section>`、`<draft-comment>` 和 `<required-cleanup>` 元素。

## 学习时长

大约 1 小时。

## 课程简介

现在，你已经学会使用DITA中的基本元素和一些常用元素了。接下来，你将学习在概念型主题中使用高级元素。

在概念性主题中，使用 `<codeblock>` 和 `<codeph>` 元素在正文中插入代码片段。使用 `<lq>` 元素可以插入长引文，并创建一个指向原文的链接。

使用 `<section>` 元素，可以将主题划分为多个小节。`<section>` 元素有两个限制条件：`<section>` 元素只能插入到 `<conbody>` 元素中，不能插入到其他 `<section>` 元素中；`<section>` 元素的后面只能插入 `<section>` 元素、`<example>` 元素或 `<conbodydiv>` 元素。

多人协作时，你可以使用 `<draft-comment>` 元素为内容片段添加批注，或者使用 `<required-cleanup>` 元素标注需要修改元素标签的内容。

本讲将介绍这些元素，并教你如何在概念型主题中使用它们。和本课中介绍的其他元素一样，这些元素不只能在概念型主题中使用，也可以在其他类型的主题中使用（比如任务型主题和参考型主题）。

!!! note "注意"
    本讲的主要内容是高级元素的基本用法。如果你想了解每个元素的详细用法，请参见 [《OASIS DITA 1.3 规范》中的概念型主题一节](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/archSpec/technicalContent/dita-concept-topic.html#dita_concept_topic)。。

## 相关资料

- [《DITA写作指南》：元素领域](https://www.oxygenxml.com/dita/styleguide/Syntax_and_Markup/c_List_of_Domains.html)
- [《OASIS DITA 1.3 规范》：代码块](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/technicalContent/codeblock.html#codeblock)
- [《OASIS DITA 1.3 规范》：行内代码](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/technicalContent/codeph.html#codeph)
- [《OASIS DITA 1.3 规范》：长引用](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/base/lq.html#lq)
- [《OASIS DITA 1.3 规范》：小节](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/base/section.html#section)
- [《OASIS DITA 1.3 规范》：批注](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/base/draft-comment.html#draft-comment)
- [《OASIS DITA 1.3 规范》：待修改的内容](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/base/required-cleanup.html#required-cleanup)