# 关系表

关系表 (`<reltable>`) 可以用来创建顺序结构和层级结构之外的主题关系。关系表位于导图之中。你可以把关系表放在导图中的任何位置，但大家一般习惯于把关系表放在主导图的末尾。

在关系表中，`<topicref>` 元素代表其引用的主题。处在同一行中的主题，属于相关主题。

下面是一个关系表示例。示例关系表中有一个标题行和一个表格行。每一行分为三列，分别是用于盛放概念型主题、参考型主题和任务型主题。

| 概念型主题         | 参考型主题                                    | 任务型主题     |
|:--------------------|:-----------------------------------------------|:----------------|
| c_about_ducks.dita | r_breedsofducks.dita <br> r_goodbreedsforpets.dita | t_feeding.dita |

使用 DITA-OT 生成文档时，DITA-OT 会根据关系表中的内容在相关主题之间创建链接。如果使用默认的 HTML 转换程序，关系表会在每个主题的末尾创建一个标题为"相关信息"的小节。

根据示例关系表，DITA-OT 会在各个主题中创建以下链接:

- 在概念型主题 `c_about_ducks.dita` 的末尾，创建指向 `r_breeedsofducks.dita`、`r_goodbreedsforpets.dita` 和 `t_feeding.dita` 的链接。
- 在参考型主题 `r_breedsofducks.dita` 的末尾，创建指向 `c_about_ducks.dita`、`r_goodbreedsforpets.dita` 和 `t_feeding.dita` 的链接。
- 在参考型主题 `r_goodbreedsforpets.dita` 的末尾，创建指向 `c_about_ducks.dita`、`r_breedsofducks.dita` 和 `t_feeding.dita` 的链接。
- 在任务型主题 `t_feeding.dita` 的末尾，创建指向 `c_about_ducks.dita`、`r_breedsofducks.dita` 和 `r_goodbreedsforpets.dita` 的链接。

!!! note "注意"
    为了更深入地说明关系表的概念，示例中还展示了一个简化写法：只要将表格行第二列中的单元格设置为 `family`，主题 `r_breedsofducks.dita` 和 `r_goodbreedsforpets.dita` 就会各自创建一个指向对方的链接。关系表中的单元格属性会在后续课程《导图和书籍导图》中详细介绍。

编写主题的时候，关系表中定义的链接关系通常不会显示出来。

视频： [DITA 关系表简介](https://www.youtube.com/watch?v=vMUxQpQvTZg)

虽然关系表可以非常复杂，但你还是要从最简单的关系表开始学起。

在主题与主题之间创建链接时，推荐使用关系表（而不推荐使用相关链接和交叉引用）的理由如下：

- 关系表中的 `<topicref>` 元素总是基于当前导图进行解析。如果关系表中定义了指向外部文件的链接，生成文档时转换程序会自动忽略该链接。这样，就可以有效避免相关链接和交叉引用可能产生的链接失效问题。
- 与相关链接和交叉引用等内联链接相比，关系表更易于维护。关系表中的每一行都可以包含多个主题，并且批量定义他们之间的关系。例如，如果你有八个相关主题，你只需要在关系表中添加一行，然后把这八个主题放进去就行了。但如果使用相关链接，你就要在八个主题中分别插入一个大同小异的 `<related-links>` 元素。如果每个主题都需要有指向其他七个主题的链接，你就需要在每个 `<related-links>` 元素中分别插入七个 `<link>` 元素。以后，当你需要删除其中的一个主题时，如果使用的是关系表，你只要修改一次就行了。但如果使用的是相关链接，你就得把其他七个主题都打开并修改一遍。