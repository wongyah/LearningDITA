# 插入选项

编写操作步骤时，你可以为用户提供多个选项。例如，使用车载音响时，用户可以选择音效模式（比如AM、FM、CD 或外接音频等）。

`<choices>` 或 `<choicetable>` 元素可以用来编写此类内容，并为其添加语义恰当的标签。

- 如果只需要对各个选项进行简短地说明，请使用 `<choices>` 元素。
- 如果需要列出各个关键词并逐个进行详细说明，请使用 `<choicetable>` 元素（本讲的后续部分将对其进行详细介绍）。

`<choices>` 元素通常以无序列表（即项目符号列表）的格式显示。`<choices>` 元素的结构和 `<ul>` 元素相似：

| `<choices>` 元素 | `<ul>` 元素 |
|---|---|
| &lt;choices&gt;<br>&nbsp;&nbsp;&lt;choice&gt;一件事情&lt;/choice&gt;<br>&nbsp;&nbsp;&lt;choice&gt;另一件事情&lt;/choice&gt;<br>&lt;/choices&gt; | &lt;ul&gt;<br>&nbsp;&nbsp;&lt;li&gt;一件事情&lt;/li&gt;<br>&nbsp;&nbsp;&lt;li&gt;另一件事情&lt;/li&gt;<br>&lt;/ul&gt; | 

一个 `<choices>` 元素中可以包含一个或多个 `<choice>` 元素。每个 `<choice>` 元素中都可以填写一个选项。任何可以在 `<li>` 元素中使用的元素，都可以在 `<choice>` 元素中使用。

## 随堂练习

1. 打开上一节使用的练习文件 `l_task_start.dita`。

2. 在第一个 `<step>` 元素的后面，再插入一个 `<step>` 元素。在 `<step>` 元素中，插入一个 `<cmd>` 元素（如果编辑器没有自动插入的话），并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE task PUBLIC "-//OASIS//DTD DITA Task//EN" "task.dtd">
    <task id="my_first_task">
    ...
          </step>
          <step>
            <cmd>挑选一本用来识别鸭子的野外手册。</cmd>
          </step>
        </steps>
      </taskbody>
    </task>
    ```

3. 在新插入的 `<cmd>` 元素后面，插入一个 `<choices>` 元素。

    ```xml
    <step>
      <cmd>挑选一本用来识别鸭子的野外手册。</cmd>
      <choices>
      </choices>
    </step>
    ```

4. 如果编辑器没有在 `<choices>` 元素中自动插入一个 `<choice>` 元素，你就手动插入一下。

    ```xml
    <step>
      <cmd>挑选一本用来识别鸭子的野外手册。</cmd>
      <choices>
        <choice>很多现代的观鸭爱好者喜欢使用《西布利观鸟指南》。</choice>
      </choices>
    </step>
    ```

    默认情况下，大多数DITA发布工具都将 `<choices>` 元素渲染为无序列表。

5. 再插入一个 `<choice>` 元素。

    ```xml
    <step>
      <cmd>挑选一本用来识别鸭子的野外手册。</cmd>
      <choices>
        <choice>很多现代的观鸭爱好者喜欢使用《西布利观鸟指南》。</choice>
        <choice>传统的观鸭爱好者喜欢使用《彼得森野外指南》。</choice>
      </choices>
    </step>
    ```
