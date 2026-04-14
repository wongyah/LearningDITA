# 插入基本元素

概念型主题中的常用元素有：

| 元素 | 说明 |
|---|---|
| `<p>` | 段落 |
| `<ul>` | 无序列表（也叫项目符号列表） |
| `<ol>` | 有序列表（也叫数字列表） |
| `<note>` | 安全信息 |

第一课 [DITA 简介](../../course01-intro/dita_intro/index.md) 中曾经介绍过这些元素。本讲简单回顾一下这些元素，并教你如何在概念型主题使用它们。

## 随堂练习

1. 打开上一节使用的练习文件 `lesson1/l_new_concept_start.dita`。

2. 在 `<conbody>` 元素中，插入一个 `<p>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="my_first_concept">
     <title>野鸭的种类</title>
     <conbody>
      <p>北美的野鸭属于下列种类之一：</p>
     </conbody>
    </concept>
    ```

    `<p>` 元素主要用来编写正文内容。它可以用在 `<conbody>` 元素中，也可以用在 `<conbody>` 元素中允许使用的很多子元素 中。

    !!! note "注意"
        使用 `<p>` 元素编写那些不需要使用语义更加明确的元素标签的正文内容。和本课中的所有示例一样，我们建议将列表项、安全信息和表格中的内容都放在 `<p>` 元素中。如果一个列表项中有好几个段落，需要使用 `<p>` 元素来分段。如果一个列表项中只有一个段落，将列表项的内容放在 `<p>` 元素中可以让它和其他列表项的结构保持一致。

    刚刚插入的 `<p>` 元素引出了下一个元素：无序列表。

3. 在 `<p>` 元素的后面，插入一个 `<ul>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="my_first_concept">
     <title>野鸭的种类</title>
     <conbody>
      ... 
      <ul>
       <li><p>钻水鸭</p></li>
       <li><p>潜水鸭</p></li>
       <li><p>海鸭</p></li>
       <li><p>树鸭</p></li>
       <li><p>天鹅</p></li>
       <li><p>鹅</p></li>
      </ul>
     </conbody>
    </concept>
    ```

    !!! note "注意"
        如果你使用的是支持DITA的编辑器，编辑器可能会为 `<ul>` 元素自动添加一个 `id` 属性。

    `<ul>` 元素是用来编写无序列表的。

    在 `<ul>` 元素中只能插入 `<li>` 元素，而且至少得插入一个。

    每个 `<li>` 元素都是无序列表中的一个列表项。在本例中，按照最佳实践，每个 `<li>` 元素中的文本都放在了 `<p>` 元素  里。

4. 在 `<ul>` 元素的后面，插入一个 `<p>` 元素（以添加引导语）和一个 `<ol>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="my_first_concept">
     <title>野鸭的种类</title>
     <conbody>
      ... 
      <p>在北美，体型最长的钻水鸭是：</p>
      <ol>
       <li><p>针尾鸭</p></li>
       <li><p>野鸭</p></li>
       <li><p>美洲黑鸭</p></li>
      </ol>
     </conbody>
    </concept>
    ```

    !!! note "注意"
        如果你使用的是支持DITA的编辑器，编辑器可能会为 `<ol>` 元素自动添加一个 `id` 属性。

    `<ol>` 元素是用来编写有序列表的。

    和 `<ul>` 元素一样，在 `<ol>` 元素中也只能添加 `<li>` 元素，而且至少得添加一个。

    在本例中，按照最佳实践，每个 `<li>` 元素中的文本都放在了 `<p>` 元素里。

    !!! note "注意"
        只有列表项必须按照一定顺序排列时，才使用 `<ol>` 元素。编写分步骤的操作说明时，使用任务型主题，不要使用 `<ol>` 元素。

5. 在 `<ol>` 元素的后面，插入一个 `<note>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="my_first_concept">
     <title>野鸭的种类</title>
     <conbody>
      ... 
      <note><p>虽然针尾鸭是体型最长的钻水鸭，但野鸭通常被认为是最大的钻水鸭，因为它更重。</p></note>
     </conbody>
    </concept>
    ```

    `<note>` 元素主要用来编写安全信息，比如在概念性主题中添加注释、警告、小心。刚刚插入的 `<note>` 元素，按照最佳实  践，里面的文本都放在了 `<p>` 元素里。

6. 对照[随堂练习的参考答案] (`lesson1/l_new_concept.dita`)，自行批改一下你刚刚完成的练习作业 `lesson1/l_new_concept_start.dita`。

## 课后练习

1. 打开文件 `lesson1/l_new_concept_exercise_start.dita`，使用该文件将以下内容转换成DITA：

    --8<-- "div_exercise_content.md:start"

    <h2 style="margin: .64em 0 .64em;">内容策略和商业目标</h2>

    应该考虑的问题如下:
     
    - 低成本文档的实际代价
    - 如何建立高效的内容开发流程?
    - 高质量文档能否降低技术支持成本?
    - 在企业范围内共享技术内容时，性价比最高的方式是什么?
    
    > **注**：忽视内容策略可能会给整个组织带来成本影响。
    {: style="margin: 1.5em 0;"}

    为了顺利实施您的项目并提高成功率，我们建议按以下顺序推进：
    
    1. 识别并访谈相关干系人。
    2. 明确实施目标，并设定衡量指标。
    3. 定义各方的角色与职责。
    4. 制定时间计划，确定关键里程碑。
    5. 构建内容创建体系。
    6. 转换遗留内容。
    7. 发布内容。
    8. 沉淀项目知识。
    9. 确保长期成功。

    --8<-- "div_exercise_content.md:end"

2. 对照[课后练习的参考答案] (`lesson1/l_new_concept_exercise.dita`)，自行批改一下你刚刚完成的练习作业 (`lesson1/l_new_concept_exercise_start.dita`)。

[随堂练习的参考答案]: sa_new_concept.md#_2
[课后练习的参考答案]: sa_new_concept.md#_3