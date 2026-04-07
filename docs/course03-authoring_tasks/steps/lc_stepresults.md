# 插入操作示例和操作结果

在操作步骤中，可以插入一个演示操作过程的示例和一个操作完成后的结果。

- 使用 `<stepxmp>` 元素为操作步骤编写示例。一个操作步骤中可以包含任意数量的 `<stepxmp>` 元素。
- 使用 `<stepresult>` 元素说明操作步骤完成后的结果。

!!! note "注意"
    `<stepxmp>` 元素编写的是当前操作步骤的操作示例。如果要编写整个任务的操作示例，请使用 `<example>` 元素（该元素将在下一讲中讲解）。

<!-- [视频：在任务型主题中插入操作示例](https://youtu.be/-9JWoT1HdWk) -->

## 随堂练习

1. 打开上一节使用的练习文件 `l_task_start.dita`。

2. 在最后一个 `<step>` 元素的后面，再插入一个 `<step>` 元素（其中包含一个 `<cmd>` 元素），并添加内容如下：

    ```xml
    ...
    <step>
      <cmd>如果你识别出了这只鸭子的种类，请将其记录在你的指南里。</cmd>
    </step>
    ...
    ```

3. 在 `<cmd>` 元素的后面，插入一个 `<stepxmp>` 元素。

    ```xml
    ...
    <step>
      <cmd>如果你识别出了这只鸭子的种类，请将其记录在你的指南里。</cmd>
      <stepxmp>
      </stepxmp>
    </step>
    ...
    ```

    `<stepxmp>` 元素中可以包含一个示例，用来进一步说明该操作步骤。

    任何可以在 `<li>` 元素中使用的元素，都可以在 `<stepxmp>` 元素中使用。如果示例中包含不可忽略的断行和空格，可以使用 `<pre>` 元素或 `<codeblock>` 元素。

4. 在 `<stepxmp>` 元素中，插入一个 `<p>` 元素，然后在 `<p>` 元素中插入一个 `<image>` 元素。

    ```xml
    ...
    <step>
      <cmd>如果你识别出了这只鸭子的种类，请将其记录在你的指南里。</cmd>
      <stepxmp>
        <p><image href="checklist.png"/></p>
      </stepxmp>
    </step>
    ...
    ```
    !!! note "注意"
        图片 `checklist.png` 保存在 `lesson2` 文件夹中。

    `<stepresult>` 元素主要用来说明操作步骤成功完成后的操作结果。

    在 `<step>` 元素中，`<stepresult>` 元素必须是最后一个元素。它的后面不能再有其他任何元素。

5. 在 `<stepxmp>` 元素的后面，插入一个 `<stepresult>` 元素。

    ```xml
    ...
      </stepxmp>
      <stepresult>
      </stepresult>
    </step>
    ...
    ```

6. 在 `<stepresult>` 元素中，插入一个 `<p>` 元素，并添加内容如下：

    ```xml
    ...
      </stepxmp>
      <stepresult>
        <p>你将拥有一条可以终生保留的观鸭记录。</p>
      </stepresult>
    </step>
    ...
    ```
