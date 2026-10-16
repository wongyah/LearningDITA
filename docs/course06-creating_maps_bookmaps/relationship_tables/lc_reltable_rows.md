# 插入关系表行

<!-- 
    本文件隶属于在 GitHub 上开源的 DITA 培训项目。
    使用许可和版权声明，请参见 LICENSE 文件和 docs/notice.md 文件。
-->

## 课堂讲解

关系表行中可以包含指向相关主题的 `<topicref>` 元素。在虚构的鸭子数据库中，可以使用 `add` 命令为数据库表添加记录。本节练习将在关系表行中添加主题引用，为与 `add` 命令有关的主题创建相关链接。

<!-- [视频：DITA 中的关系表](https://youtu.be/GHW_STBkr54) -->

## 随堂练习

1. 打开上一节使用的练习文件`maps_bookmaps_samples/samples/_reltable_start.ditamap`。

2. 在`<relheader>` 元素的后面，插入一个`<relrow>`元素。

    ```xml
    <reltable title="Ducks reltable">
    	<relheader>
    		<relcolspec type="concept"/>
    		<relcolspec type="task"/>
    		<relcolspec type="reference"/>
    	</relheader>
    	<relrow>
    	</relrow>
    </reltable>
    ```

3. 在`<relrow>`元素中，插入三个`<relcell>`元素。

    ```xml
    <relrow>
    	<relcell>
    	</relcell>
    	<relcell>
    	</relcell>
    	<relcell>
    	</relcell>
    </relrow>
    ```

    之前我们插入了三个 `<relcolspec>` 元素，表示这张关系表中有三列。

4. 在第一个 `<relcell>` 元素中，插入一个 `<topicref>` 元素，并将 `href` 属性的属性值设置为`c_writing_about_ducks.dita`。

    ```xml
    <relrow>
    	<relcell>
    		<topicref href="c_writing_about_ducks.dita"/>
    	</relcell>
    	<relcell>
    	</relcell>
    	<relcell>
    	</relcell>
    </relrow>
    ```

5. 在另外两个 `<relcell>` 元素中，也插入 `<topicref>` 元素并设置 `href` 属性如下：

    ```xml
    <relrow>
    	<relcell>
    		<topicref href="c_writing_about_ducks.dita"/>
    	</relcell>
    	<relcell>
    		<topicref href="t_adding_entry.dita"/>
    	</relcell>
    	<relcell>
    		<topicref href="r_add.dita"/>
    	</relcell>
    </relrow>
    ```

    关系表中的这一行表示，`href`指向的这三个主题之间存在关联。

6. 对照[随堂练习的参考答案] (`maps_bookmaps_samples/samples/_reltable.ditamap`)，自行批改一下你刚刚完成的练习作业 (`maps_bookmaps_samples/samples/_reltable_start.ditamap`)。

<!-- links -->
[随堂练习的参考答案]: sa_reltable.md#_2