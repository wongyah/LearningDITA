# 插入语法说明

语法说明是 API 参考手册或命令行参考手册中的关键章节，用于说明每条命令或函数调用的格式和选项。

语法说明使用文本或图形直观地表示命令或函数调用中的关键字、占位符（变量）和其他符号。语法范式通常使用方括号（`[]`）、花括号（`{}`）和竖线（`|`）表示语法规则中的可选项或必选项。语法图（也称为"铁路图"）使用线段和箭头表示语法规则中的可选项、重复项和必选项。如果你想知道语法图到底长什么样，请参阅[百度百科](https://baike.baidu.com/item/Railroad%20Diagram/19408270)。

由于语法说明的出现频率很高，参考型主题专门定制了一个用来说明语法规则的元素：`<refsyn>` 。

`<refsyn>`元素是从 `<section>` 元素定制而来的。只要能在 `<section>` 元素中使用的元素，都能在 `<refsyn>` 元素中使用，包括 `<title>` 元素。

在 `<refsyn>` 元素中插入语法说明的方法有很多，比如：

- 在 `<image>` 或 `<fig>` 元素中插入语法图（不推荐）。

- 在 `<codeblock>` 或 `<pre>`（preformatted，即预格式化）元素中插入语法范式（可接受，但只能使用极少量的额外标记）。

- 使用 `<synph>`（syntax phrase，即语法短语）元素插入语法范式（本讲中采用的方法）。

- 使用 `<syntaxdiagram>` 元素。该元素使用一些子元素来描述语法说明的各个组成部分以及它们之间的关系。这些元素可以渲染成多种不同的格式，具体取决于文档发布程序。不过，目前还没有支持 `<syntaxdiagram>` 元素的可视化编辑器，因此用起来比较麻烦。

如果想深入了解 `<synph>` 和 `<syntaxdiagram>` 的各种利弊，请参阅 Simon Bate 的博客文章：[《如何理解 DITA 中的图表?》](https://www.scriptorium.com/2013/01/perplexed-by-complex-syntax-understanding-syntax-diagrams-in-dita/)。

## 随堂练习

1. 请打开上一讲使用的练习文件 `l_reference_start.dita`。

2. 在 `<section>` 元素的后面，插入一个 `<refsyn>` 元素。

    ```xml
    ...
    <refbody>
      <section>
        <p>在鸭子数据库中，使用<cmdname>tNav</cmdname>命令可以导航到其他表格或视图。</p>
      </section>
      <refsyn></refsyn>
    </refbody>
    ...
    ```

3. 在 `<refsyn>` 元素中，插入一个用来放命令示例的 `<synph>`（syntax phrase，即语法短语）元素，并添加内容如下：

    ```xml
    ...
    <refbody>
      <section>
        <p>在鸭子数据库中，使用<cmdname>tNav</cmdname>命令可以导航到其他表格或视图。</p>
      </section>
      <refsyn><synph>-tNav tName [tView]</synph></refsyn>
    </refbody>
    ...
    ```

4. 在语法短语中，使用 `<var>`（variable，即变量）元素标记字符串"tName"。

    `<var>` 元素主要用来标记语法中的变量或占位符。在大多数文档发布程序中，`<var>` 元素中的内容会显示为斜体。

    ```xml
    ...
    <refbody>
      <section>
        <p>在鸭子数据库中，使用<cmdname>tNav</cmdname>命令可以导航到其他表格或视图。</p>
      </section>
      <refsyn><synph>-tNav <var>tName</var> [tView]</synph></refsyn>
    </refbody>
    ...
    ```
