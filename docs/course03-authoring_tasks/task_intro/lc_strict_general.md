# 严格任务主题和通用任务主题

DITA 规范定义了两种类型的任务型主题：严格任务主题和通用任务主题。

在严格任务主题中，主要元素必须按照特定的顺序排列。每个严格任务主题最多只能包含一组操作步骤。而且，操作步骤只能使用特定的元素（`<steps>` 和 `<step>`）编写。

在通用任务主题中，对元素顺序的要求不像严格任务主题那么严格。每个通用任务主题可以包含一组或多组操作步骤。只要能在 `<section>` 元素中使用的元素，差不多都能在通用任务主题的操作步骤中使用。

优先使用严格任务主题，虽然编写通用任务主题听起来好像更容易一些。理由如下：

- 一致性。严格任务主题可以让文档中的所有任务都具有相同的内容结构。
- 可靠性。由于内容结构一致，用户可以在相同的位置查找相似的信息。
- 编写难度。DITA编辑器可以向写作人员提示下一个需要插入的元素。
- 简洁性。大多数任务型主题只需要一组有序的操作步骤就行了。
- 语义性。严格任务主题中的 `<steps>` 元素和 `<step>` 元素具有很高的语义价值。

本节课重点关注严格任务主题。一旦学会使用严格任务主题中的元素，你自然就会对通用任务主题触类旁通了。

如果你想了解通用任务主题的更多信息，请参见《OASIS DITA 1.3 规范》中的[通用任务主题](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/archSpec/technicalContent/dita-generic-task-topic.html#dita_generic_task_topic)以及[`<steps-informal>` 元素](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/technicalContent/steps-informal.html#steps-informal)。