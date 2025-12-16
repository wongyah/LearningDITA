# 插入高级元素

下面是DITA中常用的一些高级元素：

| 元素 | 说明 |
|---|---|
| `<codeblock>` | 代码块。在PDF或HTML文档中，代码块通常显示为等宽字体。在`<codeblock>`元素中，可以使用换行符。 |
| `<codeph>` | 行内代码，通常是一个词语或短语。例如，你在段落中提到一个元素名称，并且希望这个元素名称以等宽字体显示，这时`<codeph>`元素就派上用场了。 |
| `<lq>` | 长引文，是指在你的内容中引用来自外部的内容，而不是添加指向原文的链接。 |

## 随堂练习

1. 为文件 `lesson4/l_concept_advanced_start.dita` 创建一个副本，然后在编辑器中打开。

    !!! note "注意"
        如果你使用的是支持DITA的编辑器，请使用文本模式，不要使用写作模式或者其他可视模式。

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_advanced">
     <title>描写鸭子</title>
     <conbody>
     </conbody>
    </concept>
    ```

2. 在 `<conbody>` 元素中，插入一个 `<codeblock>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_advanced">
     <title>描写鸭子</title>
     <conbody>
      <codeblock>
       duckdata> add entry (绿头鸭);
       1 entry added (0.05 sec)
       duckdata> _
      </codeblock>
     </conbody>
    </concept>
    ```

    `<codeblock>` 元素隔离了代码，代码中的任何字符都会显示在文档中，而且不会影响概念型主题中的DITA标签。

    在 `<codeblock>` 元素中，可以使用换行符。在本例中，`<codeblock>` 元素中的代码是使用命令行向数据库中添加记录的命令和执行结果。

    !!! note "注意"
        如果需要在 `<codeblock>` 元素中输入元素标签，请使用 `&lt;` 替代左尖括号（`<`）。如果你使用的是DITA编辑器，在写作模式或者可视模式下，你可以在 `<codeblock>` 元素中输入左尖括号。当切换到文本模式时，`<codeblock>` 元素中输入左尖括号会自动转换为 `&lt;`。

3. 在 `<conbody>` 元素的后面，插入一个 `<p>` 元素（`<p>` 元素中有一个子元素 `<codeph>`），并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_advanced">
     <title>描写鸭子</title>
     <conbody>
      ...
      </codeblock>
      <p>要在数据库中添加一条关于鸭子种类的记录，请在命令行中输入<codeph>add entry</codeph>，接着在圆括号中输入鸭子的种类，然后按回车键。</p>
     </conbody>
    </concept>
    ```

    在本例中，`<codeph>` 元素隔离了单词“add entry”，并指定这两个单词的格式为等宽字体，以此来表示它们是一条命令。

4. 在 `<p>` 元素的后面，插入一个 `<lq>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_advanced">
     <title>描写鸭子</title>
     <conbody>
      ...
      </p>
      <lq href="https://commons.digitalthoreau.org/walden/the-ponds/the-ponds-18-34/" format="html" scope="external">可比农夫家门前的池塘清澈多了！他家的鸭子在那个池塘游泳。一群纯洁的野鸭纷纷飞向这里。大自然的美，竟无一人懂得欣赏。鸟语花香，相映成趣。但世上的少男少女，谁又能真正懂得欣赏大自然的浑然天成和生机盎然之美?</lq>
     </conbody>
    </concept>
    ```

    在本例中，`<lq>` 元素引用了亨利·戴维·梭罗所著的《瓦尔登湖》中的一段话。

    `<lq>` 元素还可以创建一个指向原文的链接。在本例中，`<lq>` 元素有三个属性：指向原文地址的 `href` 属性、声明原文格式（HTML）的 `format` 属性以及声明原文来源的 `scope` 属性。
