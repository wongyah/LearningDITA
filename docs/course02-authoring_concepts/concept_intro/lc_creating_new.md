# 新建概念型主题

在概念型主题中，可以使用基本的 DITA 元素，比如段落、列表、图片、表格等。这些基本元素中的绝大多数也可以在其他类型的主题中使用（比如任务型主题和参考型主题）。唯一例外的是 `<conbody>` 元素。它只能用在概念型主题中。

一个最简单的概念型主题，至少要包含一个根元素 `<concept>`（带 `id` 属性），`<concept>` 元素中至少要包含一个 `<title>` 元素。

在 `<title>` 元素的后面，可以插入一个 `<shortdesc>` 元素或 `<abstract>` 元素，然后才是用来添加正文内容的`<conbody>`元素。

`<conbody>` 元素的内容结构很开放。也就是说，`<conbody>` 元素对子元素没有严格的顺序要求。只要是 `<conbody>` 中允许使用的元素，就可以以任何顺序出现在任何位置。不过，`<section>` 元素和 `<example>` 元素是两个例外。`<section>` 元素和 `<example>` 元素的后面只能接 `<section>` 元素、`<example> `元素或者 `<conbodydiv>` 元素。

## 随堂练习

1. 为文件 `lesson1/l_new_concept_start.dita` 创建一个副本，然后在编辑器中打开。
   
    !!! note "注意"
        如果你使用的是支持 DITA 的编辑器，请使用文本模式，不要使用写作模式或者其他可视模式。
   
    你看到的文件内容应该是这样的：
   
    ```xml
    --8<-- "sample_files/concept_topic/lesson1/l_new_concept_start.dita"
    ```

    - 第一行（以 `<?xml` 开头）是XML声明。XML声明是XML文件的一个标准组成部分。
    - 第二行是文档类型声明（即DOCTYPE声明），用来声明该文件是一个概念型主题。
    - 第三行是 `<concept>` 元素的开始标签，还带有一个属性值为 `my_first_concept` 的 `id` 属性。
    - 第四行是 `<title>` 元素，其内容是该主题的标题。
    - 第五行是 `<concept>` 元素的结束标签，表示 `<concept>` 元素在此结束。

2. 在 `<title>` 元素中，编辑标题文本如下。
   
    !!! note "注意"
        编辑元素时，要将元素内容放在开始标签和结束标签之间。
   
    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="my_first_concept">
      <title>野鸭的种类</title>
    </concept>
    ```

3. 在 `<title>` 元素的后面，插入一个 `<conbody>` 元素。
   
    !!! note "注意"
        在一个元素的后面插入新元素时，要将新元素插入到前一个元素的结束标签之后。
   
    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="my_first_concept">
      <title>野鸭的种类</title>
      <conbody>
      </conbody>
    </concept>
    ```
    
    概念型主题的实际内容将全部添加到 `<conbody>` 元素中。
