# 插入章节

<!-- 
    本文件隶属于在 GitHub 上开源的 DITA 培训项目。
    使用许可和版权声明，请参见 LICENSE 文件和 docs/notice.md 文件。
-->

## 课堂讲解

`<chapter>` 元素的结构如下：

```xml
<chapter href="filepath/filename.dita">
```

`<chapter>` 元素的结构和 `<topicref>` 元素几乎一模一样，唯一的不同点是元素名称。在 `<chapter>` 元素中，你可以使用 `href` 设置指向某个章级主题（即一级主题）的链接。

`<chapter>` 元素中可以包含以下元素：

- `<topicmeta>` 元素，可以为章级主题添加元数据。
- 任意数量的 `<topicref>` 元素。
- 任意数量的 `<mapref>` 元素。

既然使用书籍导图，你大概率会将其印制出来或 以 PDF 格式发布。所以，为书籍导图搭建层级结构时，一定要时刻想着此类发布形式的物理空间限制。如果一章里的主题级别过多，有些标题的级别可能就无法辨识了，减小字号或增加缩进可能都不再管用。读者可能会因此搞不清楚内容结构。

!!! note "注意"
    如果你想深入了解 `<chapter>` 元素，请参见《OASIS DITA 1.3 规范》：[`<chapter>` 元素](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/technicalContent/chapter.html#chapter)。

## 随堂练习

1. 打开上一节使用的练习文件 `maps_bookmaps_samples/samples/_b_ducks_start.ditamap`。

2. 在 `<booktitle>` 元素的后面，插入一个 `<chapter>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	...
    	</booktitle>
    	<chapter href="c_wild_ducks.dita">
    	</chapter>
    </bookmap>
    ```

    该 `<chapter>` 元素创建了一个指向概念型主题 `c_wild_ducks.dita` 的链接。

3. 在你刚刚插入的 `<chapter>` 元素中，再插入一个 `<topicref>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	...
    	<chapter href="c_wild_ducks.dita">
    		<topicref href="c_wild_duck_types.dita"/>
    	</chapter>
    </bookmap>
    ```

    将 `<topicref>` 元素插入到 `<chapter>` 元素中，意味着在该书籍导图中 `c_wild_duck_types.dita` 是 `c_wild_duck.dita` 这一章中的主题。

4. 在你刚刚插入的 `<topicref>` 元素的后面，再插入两个 `<topicref>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	...
    	<chapter href="c_wild_ducks.dita">
    		<topicref href="c_wild_duck_types.dita"/>
    		<topicref href="c_wild_duck_species.dita"/>
    		<topicref href="t_watching_wild_ducks.dita"/>
    	</chapter>
    </bookmap>
    ```

    现在，`c_wild_ducks.dita` 这一章中有了三个主题：`c_wild_duck_types.dita`、`c_wild_duck_species.dita` 和 `t_watching_wild_ducks.dita`。

5. 在 `<chapter>` 元素后面，再插入两个 `<chapter>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	...
    	</chapter>
    	<chapter href="c_domestic_ducks.dita">
    		<topicref href="c_duckling_growth.dita"/>
    		<topicref href="c_feeding_ducklings.dita">
    			<topicref href="c_duck_weight.dita"/>
    		</topicref>
    	</chapter>
    	<chapter href="c_duckdb.dita">
    		<topicref href="c_writing_about_ducks.dita" locktitle="yes"/>
    		<topicref href="r_tnav.dita"/>
    	</chapter>
    </map>
    ```

    现在，这张书籍导图中有了三章：`c_wild_ducks.dita`、`c_domestic_ducks.dita` 和 `c_duckdb.dita`。每一章中都有若干 `<topicref>` 元素。其中一个二级主题 `c_feeding_ducklings.dita` 中，还有一个三级主题 `c_duck_weight.dita`。

6. 对照[随堂练习的参考答案] (`maps_bookmaps_samples/samples/_b_ducks.ditamap`)，自行批改一下你刚刚完成的练习作业 (`maps_bookmaps_samples/samples/_b_ducks_start.ditamap`)。

## 课后练习

1. 打开文件 `maps_bookmaps_samples/exercises/_b_cs101_start.ditamap`，使用该文件将所有主题收集到一张书籍导图中。书籍导图的层级结构如下（仅供参考）：

    --8<-- "div_exercise_content.md:start"

    - 控制技术传播的成本
        - 低成本文档的谬误
        - 高效的技术内容开发
        - 降低技术支持成本
            - 优质的技术信息减少技术支持请求次数
            - 更高效的技术支持
        - 跨组织的内容协作
            - “协作”不等于“内容无序共享”
    - 营销与产品曝光度
        - 用技术内容支持营销
            - 强化营销信息
            - 当技术内容与营销相悖时
        - 提升产品曝光度
            - 第三方图书
        - 构建用户社区和忠诚度
            - 将游戏体验延伸到内容中
    - 法律与监管问题
        - 避免法律风险
        - 满足监管要求
            - 信息交付
            - 技术标准

    --8<-- "div_exercise_content.md:end"

2. 对照[课后练习的参考答案] (`maps_bookmaps_samples/exercises/_b_cs101.ditamap`)，自行批改一下你刚刚完成的练习作业 (`maps_bookmaps_samples/exercises/_b_cs101_start.ditamap`)。

<!-- links -->
[随堂练习的参考答案]: sa_bookmaps.md#_2
[课后练习的参考答案]: sa_bookmaps.md#_3
