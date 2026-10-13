# 前置内容、后置内容和书籍列表

## 课堂讲解

在书籍导图中，`<frontmatter>` 和 `<backmatter>` 元素都是可选元素。它们主要用来编写与文档有关的信息，位于正文之前或正文之后。`<frontmatter>` 元素必须位于 `<bookmeta>` 元素之后、第一个 `<chapter>` 元素之前。`<backmatter>` 元素必须位于最后一个 `<chapter>` 元素或者 `<appendix>` 元素之后、`<reltable>` 元素之前。

`<booklists>` 元素通常位于 `<frontmatter>` 或 `<backmatter>` 元素中。DITA 发布程序“看到”书籍列表元素，就知道应该把目录、索引等自动生成的内容放在哪里了。`<booklists>` 元素中的常用元素有：

- `<toc>`
- `<indexlist>`
- `<glossarylist>`

`<toc>` 元素的位置，就是 DITA 发布程序应该生成目录的位置。目录是根据导图的层级结构生成的。不需要任何其他信息。

`<indexlist>` 元素的位置，就是 DITA 发布程序应该生成索引的位置。索引是根据导图和主题中的 `<indexterm>` 元素生成的。如果导图和主题没有 `<indexterm>` 元素，就不会生成任何索引条目。

一个 `<glossarylist>` 元素中可以包含一个或多个 `<topicref>` 元素，也可以包含一个或多个 `<mapref>` 元素。一个 `<topicref>` 元素可以引用一个术语词条，一个 `<mapref>` 元素可以引用一张术语导图。术语词条和术语导图也可以插入到其他元素中，但放在 `<glossarylist>` 元素中，统一格式和查找内容会更加方便。

!!! note "注意"
    如果你想深入了解 `<frontmatter>` 和 `<backmatter>` 元素，请参见《OASIS DITA 1.3 规范》中的[前置内容](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/technicalContent/frontmatter.html#frontmatter)和[后置内容](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/technicalContent/backmatter.html#backmatter)。

<!-- [视频：书籍列表](https://youtu.be/Z6Df7sG4Olk) -->

## 随堂练习

1. 打开上一节使用的练习文件 `maps_bookmaps_samples/samples/_b_ducks_advanced_start.ditamap`。

2. 在 `<bookmeta>` 元素的后面，插入一个 `<frontmatter>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	...
    	</bookmeta>
    	<frontmatter>
    		<booklists>
    			<toc/>
    		</booklists>
    	</frontmatter>
    ```

3. 在最后一个 `<chapter>` 元素的后面，插入一个 `<backmatter>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	...
    	</chapter>
    	<backmatter>
    		<booklists>
    			<glossarylist>
    				<topicref href="g_duck_glossgroup.dita"/>
    			</glossarylist>
    			<indexlist/>
    		</booklists>
    	</backmatter>
    ```

    `<glossarylist>` 元素中的内容表明，术语表来自某个文件。`<indexlist>` 元素表明，DITA 发布程序应该根据导图中的主题生成索引。
