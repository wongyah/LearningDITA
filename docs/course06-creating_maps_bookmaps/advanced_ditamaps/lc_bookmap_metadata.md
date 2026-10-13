# 在书籍导图中插入元数据

## 课堂讲解

与导图相比，书籍导图的一大优势是可以添加更多元数据。在书籍导图中，可以添加所有者、书号、版权信息、出版流程和出版社等多种元数据。在书籍导图中，用来获取元数据的元素也比在导图中多得多。也就是说，即使是同一组主题，只要放在书籍导图中，语义就可以更丰富，内容可以更好找、更适合出版。

在书籍导图中，可以添加元数据的位置如下：

- 在 `<bookmap>` 元素中，使用 `<bookmeta>` 元素添加元数据。
- 在前置内容和后置内容的子元素中，使用 `<topicmeta>` 元素添加元数据。
- 在章节、主题引用和导图引用中，使用 `<topicmeta>` 元素添加元数据。

任何可以在 `<topicmeta>` 元素中使用的元素，都可以在 `<bookmeta>` 元素中使用。除此之外，`<bookmeta>` 元素中还可以使用其他一些元素，常用的有：

- `<authorinformation>`
- `<publisherinformation>`
- `<critdates>`
- `<bookid>`

在书籍导图的结构定义中，`<bookmeta>` 是可选元素。如果使用 `<bookmeta>`，必须将它插入到 `<booktitle>` 元素的后面、`<frontmatter>` 元素的前面。`<bookmeta>` 元素的结构如下：

```xml
<bookmeta>
	<authorinformation>
		<personinfo>
			<namedetails>
				<personname>
					<firstname>写作人员的名字</firstname>
					<lastname>写作人员的姓氏</lastname>
				</personname>
			</namedetails>
		</personinfo>
		<organizationinfo>
			<namedetails>
				<organizationnamedetails>
					<organizationname>公司名称</organizationname>
				</organizationnamedetails>
			</namedetails>
		</organizationinfo>
	</authorinformation>
	<critdates>
		<created date="1/1/2016"/>
		<revised modified="1/1/2025"/>
	</critdates>
	<bookid>
		<edition>4</edition>
		<booknumber>ID-9999</booknumber>
		<volume>2</volume>
	</bookid>
</bookmeta>
```

通过上面的示例，你可以直观地感受一下书籍导图中可以包含的信息有多丰富，远远超过导图。

书籍导图和导图中都可以插入 `<author>` 元素，但只有书籍导图中能插入 `<authorinformation>` 元素。`<authorinformation>` 元素可以包含的信息比 `<author>` 元素多得多，标记方式也更富有语义。

书籍导图和导图中都可以插入 `<topicmeta>` 元素，但书籍导图中有更多插入位置。例如，前置内容里的前言（`<frontmatter>` / `<preface>`）或后置内容里的术语表（`<backmatter>` / `<mapref>`）中都可以插入 `<topicmeta>` 元素。章元素、主题引用元素或导图引用元素中也可以插入 `<topicmeta>` 元素。

任何可以在导图中使用的元数据元素，都可以在书籍导图中的 `<topicmeta>` 元素中使用。除此之外，`<authorinformation>` 元素也可以插入到书籍导图里的 `<topicmeta>` 元素中。

!!! note "注意"
    如果你想深入了解 `<bookmeta>` 元素及其子元素，请参见《OASIS DITA 1.3 规范》：[`<bookmeta>` 元素](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/technicalContent/bookmeta.html#bookmeta)。

## 随堂练习

1. 为 `maps_bookmaps_samples/samples/_b_ducks_advanced_start.ditamap` 文件复制一个副本，然后在编辑器中打开。

2. 在 `<booktitle>` 元素的后面，插入一个 `<bookmeta>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	...
    	</booktitle>
    	<bookmeta>
    		<author>王五</author>
    		<bookrights>
    			<copyrfirst>
    				<year>2023</year>
    			</copyrfirst>
    			<copyrlast>
    				<year>2025</year>
    			</copyrlast>
    			<bookowner>
    				<organization>某某公司</organization>
    			</bookowner>
    		</bookrights>
    	</bookmeta>
    </bookmap>
    ```

    刚刚插入的 `<bookmeta>` 元素为书籍导图添加了以下元数据：

    - 这本书是王五写的。
    - 版权期限为 2023-2025 年。
    - 该书由某某公司出版发行。

3. 在指向 `c_wild_ducks.dita` 文件的 `<chapter>` 元素中，插入一个 `<topicmeta>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	...
    	</bookmeta>
    	<chapter href="c_wild_ducks.dita">
    		<topicmeta>
    			<category>野鸭</category>
    		</topicmeta>
    		...
    	</chapter>
    </bookmap>
    ```

    刚刚插入的 `<topicmeta>` 元素为章节添加了以下元数据：

    - 这一章是写野鸭的。
