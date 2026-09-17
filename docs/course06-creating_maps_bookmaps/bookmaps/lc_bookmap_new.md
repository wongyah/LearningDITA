<!-- 
    本文件隶属于在 GitHub 上开源的 DITA 培训项目。
    使用许可和版权声明，请参见 LICENSE 文件和 docs/notice.md 文件。
-->

# 新建书籍导图

## 课堂讲解

书籍导图是基于导图定制的主题类型。它的根元素（即主题引用和导图引用的容器）不是 `<map>`，而是 `<bookmap>`。一个最简单的书籍导图，至少要包含一个根元素 `<bookmap>`。书籍导图（`<bookmap>`）中可以包含以下元素：

- `<booktitle>` 元素，可以为书籍导图添加标题（比如“某某产品使用手册”）。
- `<bookmeta>` 元素，可以为书籍导图添加元数据。
- `<frontmatter>` 元素，可以为书籍导图添加目录、前言等前置内容。
- 任意数量的 `<chapter>` 元素。每个 `<chapter>` 元素都包含一个指向一级主题的链接。每个 `<chapter>` 元素中还可以包含任意数量的 `<topicref>` 元素作为子元素。
- `<backmatter>` 元素，可以为书籍导图添加索引、术语表等后置内容。

!!! note "注意"
    如果你想深入了解 `<bookmap>` 元素，请参见《OASIS DITA 1.3 规范》：[`<bookmap>` 元素](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/technicalContent/bookmap.html#bookmap)。

## 随堂练习

1. 为 `maps_bookmaps_samples/samples/_b_ducks_start.ditamap` 文件复制一个副本，然后在编辑器中打开。

    !!! note "注意"
        如果你使用的是支持 DITA 的编辑器，请使用文本模式，不要使用写作模式或者其他可视模式。

    你看到的文件内容应该是这样的：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    </bookmap>
    ```

    第一行（以 `<?xml` 开头）是XML声明。XML声明是XML文件的一个标准组成部分。

    第二行是文档类型声明（即DOCTYPE声明），用来声明该文件是一张书籍导图。

    第三行是 `<bookmap>` 元素的开始标签，还带有一个属性值为 `ducks` 的 ID。

    第四行是 `<bookmap>` 元素的结束标签，表示 `<bookmap>` 元素在此结束。

2. 在 `<bookmap>` 元素中，插入一个 `<booktitle>` 元素如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	<booktitle>
    	</booktitle>
    </bookmap>
    ```

3. 在 `<booktitle>` 元素中，插入一个 `<mainbooktitle>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	<booktitle>
    		<mainbooktitle>书名</mainbooktitle>
    	</booktitle>
    </bookmap>
    ```

    现在，书籍导图的基本结构已经搭建好了。你可以往里面添加章节了！。
