# 新建关系表

<!-- 
    本文件隶属于在 GitHub 上开源的 DITA 培训项目。
    使用许可和版权声明，请参见 LICENSE 文件和 docs/notice.md 文件。
-->

## 课堂讲解

关系表位于 `<reltable>` 元素中。`<reltable>` 元素的父元素，不是 `<map>` 元素就是 `<bookmap>` 元素。一张导图或书籍导图可以包含多个 `<reltable>` 元素。

在导图和书籍导图中，`<reltable>` 元素的位置是不同的：

- 在导图中，`<reltable>` 元素可以位于任何位置。不过，大家通常把它放在导图的末尾（即最后一个 `<topicref>` 元素的后面）。
- 在书籍导图中，`<reltable>` 元素必须位于末尾（即 `</bookmap>` 标签的前面）。

关系表中的每一列都包含一类相似的信息。在关系表的标题行（即 `<relheader>`）中，你可以使用 `<relcolspec>` 为每一列定义一个信息类型。

最常见的做法是，使用 `<relcolspec>` 元素定义三个关系表列：概念型主题列（即 `concept`）、任务型主题列（即 `task`）和参考型主题列（即 `reference`）。当然，可以放进关系表中的信息类型不只这些。

## 随堂练习

1. 为 `maps_bookmaps_samples/samples/_reltable_start.ditamap` 文件创建一个副本，然后在编辑器中打开。

    在这张导图中，已经填写好 `<topicref>` 元素了。

2. 在导图的末尾（`<map>`元素的结束标签之前），插入一个`<reltable>`元素。

    ```xml
    	...
    	</topichead>
    	</topicref>
    	<mapref href="g_duck_glossorg.ditamap" format="ditamap"/>
    	<reltable title="鸭子关系表">
    	</reltable>
    </map>
    ```

    注意一下，你可以使用 `<reltable>` 元素的 `title` 属性说明关系表的用途，但该标题永远不会显示在发布后的文档中。

3. 在关系表中，插入一个 `<relheader>` 元素，再在 `<relheader>` 元素中插入三个 `<relcolspec>`元素：

    ```xml
    <reltable title="鸭子关系表">
    	<relheader>
    		<relcolspec/>
    		<relcolspec/>
    		<relcolspec/>
    	</relheader>
    </reltable>
    ```

4. 为每个 `<relcolspec>` 元素添加一个 `type`，属性值分别设置为 `concept`、`task` 和 `reference`。

    ```xml
    <relheader>
    	<relcolspec type="concept"/>
    	<relcolspec type="task"/>
    	<relcolspec type="reference"/>
    </relheader>
    ```

    在下一节中，继续填写 `<reltable>` 元素。
