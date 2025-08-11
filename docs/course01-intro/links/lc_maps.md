# 导图

导图可以将内容组织在一起，形成可交付的文档。导图相当于目录，可以用来安排主题在文档中的前后顺序和层次结构。如果使用导图生成了PDF文档或帮助系统，读者在阅读文档时看到的内容结构就是按照导图中的主题顺序和层次结构生成的。

一般情况下，一张导图中只添加当前文档需要的主题，而不是将所有主题都添加进来。还有，一个主题可以添加到多个导图中。在 DITA 中，这也是内容复用的一种方式。

视频： [DITA导图示例](https://www.youtube.com/watch?v=I_yvE9_ECRw)

导图中的常用元素有：

- `<topicref>` 元素，可以用来创建指向特定主题的引用。
- `<mapref>` 元素，可以用来创建指向其他导图的引用。

在导图中，`<topicref>` 的前后顺序就是主题的前后顺序。`<topicref>` 的嵌套关系，就是主题的层次结构。下面是一个示例：

```xml
<map>
    <title>我的第一张导图</title>
    <topicref href="ducks.dita">
        <topicref href="range.dita"/>
        <topicref href="size.dita"/>
        <topicref href="nests.dita"/>
    </topicref>
</map>
```

为了便于查看，示例中的代码设置了缩进。这个示例中的重点是，第一个 `<topicref>` 元素中嵌套了三个 `<topicref>` 子元素。这就意味着，`ducks.dita` 主题有三个子主题，即 `range.dita`、`size.dita` 和 `nests.dita`。这张导图相当于下面的目录：

- 鸭子（Ducks）
  - 栖息地（Range）
  - 体型（Size）
  - 巢穴（Nests）

在导图中，不仅可以引用主题，也可以引用其他导图。引用导图时，子导图中通常是相互关联的一组主题。例如，你可以为书中的每一章都创建一个导图，然后再将这些章节导图添加到书籍总导图中。

引用导图时，应该使用 `<mapref>` 元素，而不是 `<topicref>` 元素。假如鸭子导图只是文档中的一个章节，你就可以创建一张总导图（父导图），然后在总导图中引用鸭子导图。像这样：

```xml
<topicref href="fish.dita">
<topicref href="shorebirds.dita">
<mapref href="ducks.ditamap" format="ditamap"/>
```

视频： [在导图中复用导图](https://www.youtube.com/watch?v=5gXZN505XFQ)
