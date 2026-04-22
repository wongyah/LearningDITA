# 插入选项表

选择表是一个两列的表格。表格的第一列是选项（比如关键字、命令行参数或参数值）。表格的第二列是对选项的详细说明。在详细说明中，可以包含多个段落、列表、甚至图片。

`<choicetable>` 元素中的常用元素有：

`<chhead>`
: 选项表的标题行。`<chhead>` 元素是可选元素。它有两个子元素：`<choptionhd>` 元素和 `<chdeschd>` 元素。一个 `<choicetable>` 元素中最多只能包含一个 `<chhead>` 元素。

`<choptionhd>`
: 选项表第一列（即选项列）的列标题。根据最佳实践，列标题的文本应该放在 `<p>` 元素中。

`<chdeschd>`
: 选项表第二列（即详细说明列）的列标题。根据最佳实践，详细说明列的文本应该放在 `<p>` 元素中。

`<chrow>`
: 选项表的数据行。`<chrow>` 元素有两个子元素：`<choption>` 元素和 `<chdesc>` 元素。一个 `<choicetable>` 元素中可以包含一个或多个 `<chrow>` 元素。

`<choption>`
: 数据行中的选项。根据最佳实践，选项的文本应该放在 `<p>` 元素中。

`<chdesc>`
: 数据行中的详细说明。根据最佳实践，详细说明的文本应该放在 `<p>` 元素中。`<chdesc>` 元素中可以包含多个子元素。

<!-- [视频：在任务型主题中创建选项表](https://youtu.be/nBua0_PDfFA)演示如何使用 [Oxygen XML Editor](https://www.oxygenxml.com/) 的选项表向导。 -->

## 随堂练习

1. 打开上一节使用的练习文件 `l_task_start.dita`。

2. 在包含 `<choices>` 元素的 `<step>` 元素后面，再插入一个 `<step>` 元素（其中包含一个 `<cmd>` 元素），并添加内容如下：

    ```xml
    <step>
      <cmd>寻找一些质量好的光学仪器</cmd>
    </step>
    ```

3. 在 `<cmd>` 元素的后面，插入一个 `<choicetable>` 元素，并添加子元素如下：

    ```xml
    <step>
      <cmd>寻找一些质量好的光学仪器</cmd>
      <choicetable>
        <chrow>
          <choption></choption>
          <chdesc></chdesc>
        </chrow>
        <chrow>
          <choption></choption>
          <chdesc></chdesc>
        </chrow>
      </choicetable>
    </step>
    ```

    `<choicetable>` 中的每一行，都需要插入一个 `<chrow>` 元素。每个 `<chrow>` 元素中都要插入两个必选的子元素：用来放选项的 `<choption>` 元素和用来对选项进行详细说明的 `<chdesc>` 元素。按照标准用法，`<choption>` 元素中只写几个单词（通常是一个），而 `<chdesc>` 元素中可以写多个句子，甚至段落（即 `<p>` 元素）。

    在 `<choicetable>` 元素中，可以包含一个用来添加列标题的标题行（`<chhead>`）。`<chhead>` 元素是可选元素。

4. 在选项表第一行的前面，插入一个 `<chhead>` 元素，并添加子元素如下：

    ```xml
    <step>
      <cmd>寻找一些质量好的光学仪器。</cmd>
      <choicetable>
        <chhead>
          <choptionhd></choptionhd>
          <chdeschd></chdeschd>
        </chhead>
        <chrow>
          <choption></choption>
          <chdesc></chdesc>
        </chrow>
        ...
      </choicetable>
    </step>
    ```

    `<choptionhd>` 元素主要用来为选项列添加列标题。`<chdeschd>` 元素主要用来为详细说明列添加列标题。

5. 为 `<chhead>` 元素及其子元素添加内容如下：

    ```xml
    ...
    <chhead>
      <choptionhd>
        <p>种类</p>
      </choptionhd>
      <chdeschd>
        <p>优点</p>
      </chdeschd>
    </chhead>
    ...
    ```

6. 为 `<chrow>` 元素及其子元素添加内容如下：

    ```xml
    ...
    <chrow>
      <choption>
        <p>双筒望远镜</p>
      </choption>
      <chdesc>
        <p>视场大，便于快速观察。</p>
      </chdesc>
    </chrow>
    <chrow>
      <choption>
        <p>鉴识望远镜</p>
      </choption>
      <chdesc>
        <p>倍率高，聚光性能好。</p>
      </chdesc>
    </chrow>
    ...
    ```
