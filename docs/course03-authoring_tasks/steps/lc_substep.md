# 插入子步骤

编写操作流程时，你可能需要对其中的某项操作进行更加详细的说明。在这种情况下，你可以在 `<step>` 元素中插入一个 `<substeps>` 元素。

一个 `<substeps>` 元素中可以包含一个或多个 `<substep>` 元素。`<substep>` 元素的内容结构与 `<step>` 元素差不多。每个 `<substep>` 元素中能且只能包含一个 `<cmd>` 元素。

在DITA中，操作流程最多只能分为两个层级。第一层级的操作流程使用 `<steps>` 元素；第二层级的操作流程使用 `<substeps>` 元素；不允许插入第三层级的操作流程。当你想插入第三层级的操作流程时，不妨重新考虑一下整个操作流程的层级安排。或许，将这个操作流程拆分成一系列单独的任务型主题会更好。当你在子步骤中进行大量的细节说明时，处理方式同上。

<!-- [视频：在任务型主题中插入子步骤](https://youtu.be/1HDXrdB5y4w) -->

## 随堂练习

1. 打开上一节使用的练习文件 `l_task_start.dita`。

2. 在最后一个 `<step>` 元素的后面，再插入一个 `<step>` 元素（其中包含一个 `<cmd>` 元素），并添加内容如下：

    ```xml
    <step>
      <cmd>去观看鸭子。</cmd>
    </step>
    ```

3. 在 `<cmd>` 元素的后面，插入一个 `<substeps>` 元素。

    ```xml
    <step>
      <cmd>去观看鸭子。</cmd>
      <substeps>
      </substeps>
    </step>
    ```

    一个 `<step>` 元素中可以包含一个或多个 `<substeps>` 元素。但是，`<substeps>` 元素不能自嵌套，只能在同一层别按顺序插入。

4. 如果编辑器没有在 `<substeps>` 元素中自动插入一个 `<substep>` 元素及其子元素 `<cmd>`，现在手动插入一个。

    ```xml
    <step>
      <cmd>去观看鸭子。</cmd>
      <substeps>
        <substep>
          <cmd></cmd>
        </substep>
      </substeps>
    </step>
    ```

5. 在 `<substep>` 元素的子元素 `<cmd>` 中添加内容如下：

    ```xml
    <step>
      <cmd>去观看鸭子。</cmd>
      <substeps>
        <substep>
          <cmd>四处走走。</cmd>
        </substep>
      </substeps>
    </step>
    ```

    `<step>` 元素中允许插入的可选元素，也可以插入到 `<substep>` 元素中，比如 `<info>` 元素。但是，一个 `<substeps>` 元素不能插入到另一个 `<substep>` 元素中。

6. 在 `<substep>` 元素的后面，再插入两个 `<substep>` 元素，并添加内容如下：

    ```xml
    <step>
      <cmd>去观看鸭子。</cmd>
      <substeps>
        <substep>
          <cmd>四处走走。</cmd>
        </substep>
        <substep>
          <cmd>如果你看到一只鸭子，停下来。</cmd>
        </substep>
        <substep>
          <cmd>识别一下这只鸭子的种类。</cmd>
        </substep>
      </substeps>
    </step>
    ```
