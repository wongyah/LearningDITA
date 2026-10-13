# 在书籍导图中插入章节标题

## 课堂讲解

在导图中，你可以使用 `<topichead>` 元素将一个或多个主题划分到一个章节中，并为该章节添加标题。使用 `<topichead>` 元素添加的章节标题，会显示在正文中。如果有目录的话，也会显示在目录中。在 `<topichead>` 元素中，`<navtitle>` 元素是必选元素。

如果要将若干主题划分成一个章节，但不想为章节标题单独创建一个主题，`<topichead>` 元素就会派上用场了！在这样的章节中，主题之间通常没有明确的层级关系，仅在当前上下文中存在某些关联。

!!! note "注意"
    如果你想深入了解 `<topichead>` 元素，请参见《OASIS DITA 1.3 规范》：[章节标题](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/base/topichead.html#topichead)。

## 随堂练习

1. 打开上一节使用的练习文件 `maps_bookmaps_samples/samples/_b_ducks_advanced_start.ditamap`。

2. 在指向 `t_create_table.dita` 主题的 `<topicref>` 元素前面，插入 `<topichead>` 元素的开始标签。在指向 `t_modify_table.dita` 主题的 `<topicref>` 元素后面，插入 `<topichead>` 元素的结束标签。

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	...
    	<chapter href="c_duckdb.dita">
    		<topichead>
    			<topicref href="t_create_table.dita">
    			<topicref href="t_adding_entry.dita">
    			<topicref href="t_modify_entry.dita">
    			<topicref href="t_deleting_entry.dita">
    			<topicref href="t_queries.dita">
    			<topicref href="t_modify_table.dita">
    		</topichead>
    		...
    ```

3. 在 `<topichead>` 元素的开始标签后面，插入一个 `<topicmeta>` 元素，然后再插入一个子元素 `<navtitle>`，如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE bookmap PUBLIC "-//OASIS//DTD DITA BookMap//EN" "bookmap.dtd">
    <bookmap id="ducks">
    	...
    	<chapter href="c_duckdb.dita">
    		<topichead>
    			<topicmeta>
    				<navtitle>普通任务</navtitle>
    			</topicmeta>
    			<topicref href="t_create_table.dita">
    			<topicref href="t_adding_entry.dita">
    			<topicref href="t_modify_entry.dita">
    			<topicref href="t_deleting_entry.dita">
    			<topicref href="t_queries.dita">
    			<topicref href="t_modify_table.dita">
    		</topichead>
    		...
    ```

<!-- 4. 对照[随堂练习的参考答案] (`maps_bookmaps_samples/samples/_b_ducks_advanced.ditamap`)，自行批改一下你刚刚完成的练习作业 (`maps_bookmaps_samples/samples/_b_ducks_advanced_start.ditamap`)。 -->

<!-- links -->
[随堂练习的参考答案]: sa_advanced_ditamaps.md#_2
