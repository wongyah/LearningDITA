# 新建参考型主题

一个最简单的参考型主题，至少要包含一个根元素 `<reference>`（带 `id`），`<reference>` 元素中至少要包含一个 `<title>` 元素。

在 `<title>` 元素的后面，可以插入一个 `<shortdesc>` 元素或 `<abstract>` 元素，然后才是用来添加正文内容的 `<refbody>` 元素。基于内容结构设计，`<refbody>` 元素中只能插入少数几种元素。换句话说，参考型主题的内容灵活性不如概念型主题。

以前介绍过的很多元素也可以在参考型主题的正文中使用：`<table>`、`<fig>`、`<image>`、`<example>` 和 `<section>`。在 `<refbody>` 元素中，通常使用 `<section>` 元素为正文划分小节，比如命令描述、使用指南、错误代码等。此外，`<refbody>` 元素中还可以插入两个参考型主题中特有的元素：`<refsyn>`（reference syntax，即参考语法）和 `<properties>`。

在参考型主题的正文中，上述元素可以以任意顺序插入，且数量不限。

在 `<example>`、`<section>`、和 `<refsyn>` 元素中，均可以包含一个 `<title>` 元素。这样，你就可以在参考型主题中划分小节。如有必要，文档发布程序可以为 `<properties>` 自动生成并插入专属标题。

<!-- [视频：创建参考型主题](https://youtu.be/B3FVRhrfwkA) -->

## 随堂练习

1. 为文件 `l_reference_start.dita` 创建一个副本，然后在编辑器中打开。

    !!! note "注意"
        如果你使用的是支持DITA的编辑器，请使用文本模式，不要使用写作模式或者其他可视模式。

    你看到的文件内容应该是这样的：

    ```xml
    --8<-- "sample_files/reference_topic/l_reference_start.dita"
    ```

    - 第一行（以 `<?xml` 开头）是XML声明。XML 声明是 XML 文件的一个标准组成部分。
    - 第二行是文档类型声明（即 DOCTYPE 声明），用来声明该文件是一个参考型主题。对主题内容进行验证时，程序会用到该信息。每个主题类型的文档类型（即 DOCTYPE）都各不相同，包括通用任务主题。
    - 第三行是 `<reference>` 元素的开始标签。
    - 第四行是 `<title>` 元素。

2. 在 `<title>` 元素中，编辑标题文本如下。

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE reference PUBLIC "-//OASIS//DTD DITA Reference//EN" "reference.dtd">
    <reference id="my_first_ref">
      <title>tNav</title>
    </reference>
    ```

3. 在 `<title>` 元素的后面，插入一个 `<refbody>` 元素。

    参考型主题的正文内容将全部添加到 `<refbody>` 元素中。

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE reference PUBLIC "-//OASIS//DTD DITA Reference//EN" "reference.dtd">
    <reference id="my_first_ref">
      <title>tNav</title>
      <refbody>
      </refbody>
    </reference>
    ```

4. 在 `<refbody>` 元素中，插入一个 `<section>` 个元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE reference PUBLIC "-//OASIS//DTD DITA Reference//EN" "reference.dtd">
    <reference id="my_first_ref">
      <title>tNav</title>
      <refbody>
        <section>
          <p>在鸭子数据库中，使用<cmdname>tNav</cmdname>命令可以导航到其他表格或视图。</p>
        </section>
      </refbody>
    </reference>
    ```

    !!! note "注意"
        `<cmdname>`（command name，即命令名称）元素来自编程领域，可以用来表示软件里的命令名称。如果你想深入了解编程领域，请参见 《OASIS DITA 1.3 规范》中的[编程元素](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/containers/pr-d.html#progd)。
