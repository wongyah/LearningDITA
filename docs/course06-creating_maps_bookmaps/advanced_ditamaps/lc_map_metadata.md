# 在导图中插入元数据

## 课堂讲解

主题中的元数据，可以为主题添加主题信息。导图中的元数据，既可以为导图添加导图信息，也可以为主题引用或导图引用添加信息。

你可以使用 `<topicmeta>` 元素为导图添加元数据。导图的根元素 `<map>`、导图中的任何一个 `<topicref>` 或 `<mapref>` 元素中都可以插入 `<topicmeta>` 元素。

在导图的根元素 `<map>` 中插入 `<topicmeta>` 元素，可以为导图添加导图信息，使搜索和过滤更加方便。通常，导图的元数据不会出现在发布后的文档中。但是，它可以影响文档发布程序，比如指定文档发布过程中生成封面的方式。

在 `<topicref>` 或 `<mapref>` 元素中插入 `<topicmeta>` 元素，可以为主题引用添加主题信息，或者为导图引用添加导图信息。这些信息甚至可以覆盖这些主题或导图自带的元数据。例如，如果一个主题中包含 `<prolog>` 或 `<shortdesc>` 元素，导图中引用该主题的 `<topicref>` 元素中也包含 `<prolog>` 或 `<shortdesc>` 元素，那么 `<topicref>` 元素中的元数据优先级更高。

`<topicmeta>` 元素中可以插入的元数据元素很多，常用的有：

- `<navtitle>`
- `<author>`
- `<copyright>`
- `<category>`

`<topicmeta>` 元素中也可以插入 `<metadata>` 元素，虽然 `<metadata>` 元素本身也可以插入上面那些元数据元素。

`<topicmeta>` 元素的结构如下：

```xml
<topicmeta>
	<navtitle>导航标题</navtitle>
	<author>写作人员姓名</author>
	<copyright>
		<copyryear year="20XX"/>
		<copyrholder>公司名称</copyrholder>
	</copyright>
	<category>类别</category>
</topicmeta>
```

!!! note "注意"
    如果你想深入了解 `<topicmeta>` 元素及其子元素，请参见《OASIS DITA 1.3 规范》：[`<topicmeta>` 元素](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/base/topicmeta.html#topicmeta)。

## 随堂练习

1. 为 `maps_bookmaps_samples/samples/_m_ducks_advanced_start.ditamap` 文件复制一个副本，然后在编辑器中打开。

    你看到的文件开头应该是这样的（文件内容很长，这里只展示一小部分）：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
    <map id="ducks">
    	<title>鸭子</title>
    	<topicref href="c_wild_ducks.dita">
    		<topicref href="c_wild_duck_types.dita"/>
    		<topicref href="c_wild_duck_species.dita"/>
    		<topicref href="c_habitats.dita"/>
    		<topicref href="t_watching_wild_ducks.dita"/>
    	</topicref>
    	<topicref href="c_domestic_ducks.dita">
    		<topicref href="c_duckling_growth.dita"/>
    		<topicref href="c_housing.dita"/>
    		...
    ```

2. 在 `<title>` 元素的后面，插入一个 `<topicmeta>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
    <map id="ducks">
    	<title>鸭子</title>
    	<topicmeta>
    		<critdates>
    			<created date="2026-09-17"/>
    		</critdates>
    		<category>样本</category>
    	</topicmeta>
    	...
    </map>
    ```

    刚刚插入的 `<topicmeta>` 元素为导图添加了以下元数据：

    - 导图的创建日期：2026 年 09 月 17 日
    - 这张导图是一张样图。

3. 在指向 `c_duckdb.dita` 文件的 `<topicref>` 元素中，插入一个 `<topicmeta>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
    <map id="ducks">
    	<title>鸭子</title>
    	...
    	<topicref href="c_duckdb.dita">
    		<topicmeta>
    			<audience type="user" experiencelevel="expert"/>
    		</topicmeta>
    		<topicref href="c_writing_about_ducks.dita"/>
    		...
    	</topicref>
    	...
    </map>
    ```

    刚刚插入的 `<topicmeta>` 元素为主题添加了以下元数据：

    - 本节内容的目标读者是本产品的用户，不是管理员或普通读者。
    - 本节内容的目标读者是专家级用户。

4. 在指向 `g_duck_glossorg.ditamap` 文件的 `<mapref>` 元素中，插入一个 `<topicmeta>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
    <map id="ducks">
    	<title>鸭子</title>
    	...
    	<mapref href="g_duck_glossorg.ditamap" format="ditamap">
    		<topicmeta>
    			<searchtitle>关于鸭子的术语</searchtitle>
    		</topicmeta>
    	</mapref>
    </map>
    ```

    刚刚插入的 `<topicmeta>` 元素为子导图添加了以下元数据：

    - 如果有人通过搜索工具找到该主题，搜索结果页面应该显示标题“关于鸭子的术语”，而不是主题文件中的标题。

5. 对照[随堂练习的参考答案] (`maps_bookmaps_samples/samples/_m_ducks_advanced.ditamap`)，自行批改一下你刚刚完成的练习作业 (`maps_bookmaps_samples/samples/_m_ducks_advanced_start.ditamap`)。

<!-- links -->
[随堂练习的参考答案]: sa_advanced_ditamaps.md#_2
