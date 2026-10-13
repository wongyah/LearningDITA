# 为书籍导图设置导航标题

## 课堂讲解

在一张导图中，可能会有个别主题的标题显得不太协调，尤其是复用的主题。例如，其他任务型主题都使用动宾短语做标题（比如“安装操作系统”），但某个复用的主题却使用主谓短语做标题（比如“操作系统安装”）。在这种情况下，你可以使用 `<navtitle>` 元素为该主题设置一个导航标题，使其与其他主题的标题风格保持统一。

在一些比较老的导图或书籍导图中，你可能会看到一些元素设置了 `navtitle` 属性（比如 `<topicref>` 元素）。现在，`navtitle` 属性已经过时了，推荐使用 `<navtitle>` 元素。

!!! note "注意"
    如果你想深入了解 `<navtitle>` 元素，请参见《OASIS DITA 1.3 规范》：[导航标题](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/base/navtitle.html#navtitle)。

## 随堂练习

1. 打开上一节使用的练习文件 `maps_bookmaps_samples/samples/_b_ducks_advanced_start.ditamap`。

2. 找到引用 `r_tnav.dita` 主题的 `<topicref>` 元素，将该元素的 `locktitle` 属性设置为 `yes`，如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	...
    	<topicref href="r_tnav.dita" locktitle="yes"/>
    	...
    </bookmap>
    ```

    !!! note "注意"
        要让 `<topicref>` 元素的导航标题生效，必须将它的 `locktitle` 属性设置为 `yes`。如果不设置 `locktitle` 属性或将其设置为 `no`，导航标题不会生效。

3. 将 `<topicref>` 元素的自闭合标签（`<topicref … />`）修改为独立的开始标签和结束标签（`<topicref ...></topicref>`）。

    ```xml
    <topicref href="r_tnav.dita" locktitle="yes">
    </topicref>
    ```

4. 在 `<topicref>` 元素中，插入一个 `<topicmeta>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	...
    	<topicref href="r_tnav.dita" locktitle="yes">
    		<topicmeta>
    			<navtitle>tNav 命令</navtitle>
    		</topicmeta>
    	</topicref>
    	...
    </bookmap>
    ```

    现在，你已经设置好导航标题了！在目录中，该主题的标题将显示为“tNav 命令”，而不是正文中的“tNav”。

5. 对照[随堂练习的参考答案] (`maps_bookmaps_samples/samples/_b_ducks_advanced.ditamap`)，自行批改一下你刚刚完成的练习作业 (`maps_bookmaps_samples/samples/_b_ducks_advanced_start.ditamap`)。

## 课后练习

1. 打开上一节使用的练习文件 `maps_bookmaps_samples/exercises/_b_cs101_start.ditamap`，使用该文件为书籍导图添加元数据、前置内容和后置内容。书籍导图的层级结构如下（仅供参考）：

    --8<-- "div_exercise_content.md:start"

    - **作者：** Sarah O'Keefe
    - **作者：** Alan S. Pringle
    - **出版社：** Scriptorium 出版服务公司
    - **创建时间：** 2012
    - **修订时间：** 2014
    - **目录：**
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
    - **索引**

    --8<-- "div_exercise_content.md:end"

2. 对照[课后练习的参考答案] (`maps_bookmaps_samples/exercises/_b_cs101_advanced.ditamap`)，自行批改一下你刚刚完成的练习作业 (`maps_bookmaps_samples/exercises/_b_cs101_start.ditamap`)。

<!-- links -->
[随堂练习的参考答案]: sa_advanced_ditamaps.md#_2
[课后练习的参考答案]: sa_advanced_ditamaps.md#_3
