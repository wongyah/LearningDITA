# 使用导图管理术语词条

通常，术语词条主题会聚中存放在一个或多个 DITA 导图中。导图的内容和结构，主要取决于实际需求以及 DITA 发布程序的功能。如果您的发布程序功能强大，术语导图的结构会更灵活。

最简单的方法是，使用 `<topicref>` 元素将所有术语词条收集到一张导图中。

```xml
<map>
  <title>关于鸭子的术语</title>
  <topicref href="g_acorns.dita"/>
  <topicref href="g_aythyinae.dita"/>
  <topicref href="g_canvasback.dita"/>
  ... 
</map>
```

如果按照字母顺序排列术语，使用标准的 DITA 发布程序就可以生成术语表，不需要专门排序。

!!! note "注意"
    在术语导图中，通常使用 `<title>` 元素插入一个标题，方便写作人员查找。如果将术语导图作为其他导图的子导图，合并导图时术语导图的标题会被忽略。

在其他导图中，可以将术语导图引用为子导图（使用 `<topicref>` 或 `<mapref>` 元素）。

然而，现实世界往往比较复杂，不是用一张导图将所有词条拉进来就行了。实施 DITA 时，最好让样式表开发人员选择术语的管理方式，使它既能满足您的需求，又能以合适的形式发布。

关于术语的管理和发布，需要注意的事项如下：

- 如果您的内容来自多个不同的团队，每个团队可能都有一套自己的术语词条。文档发布时，所有术语词条都需要合并在一起（并排序）。
- 同理，不同的产品线可能也都有自己的术语表。这些术语表可能也需要合并在一起，具体取决于实际情况。

需要维护多张术语导图并在发布时合并的情况还有很多，比如：

- 发布程序可能需要将术语分组主题中的词条合并到自己的术语表中。
- 如果需要翻译，术语词条很有可能需要根据目标语言的习惯重新排序。如果发布程序可以自动为术语词条重新排序，那本地化团队就省心了。

所有这些情况，其实都可以通过精心设计的发布程序来解决。

## 随堂练习

1. 为文件 `l_glossorg_start.ditamap` 创建一个副本，然后在编辑器中打开。

    !!! note "注意"
        在 XML编辑器中，导图文件与 DITA 文件的默认打开位置通常是不一样的。如果要在编辑区打开导图文件，可能需要一些额外的操作。

    你看到的文件内容应该是这样的：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
    <map>
      <title></title>
    </map>
    ```

2. 在 `<title>` 元素中，为导图输入一个标题如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
    <map>
      <title>关于鸭子的术语</title>
    </map>
    ```

3. 在 `<title>` 元素的后面，插入一个 `<topicref>` 元素。

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
    <map>
      <title>关于鸭子的术语</title>
      <topicref href="l_glossentry.dita"/>
    </map>
    ```

    在术语词条的随堂练习中，如果你为练习文件起的文件名不是 `l_glossentry.dita`，请使用你的文件名替换上面代码中的 `l_glossentry.dita`。

4. 如果你还创建了其他术语词条主题，请使用 `<topicref>` 元素将这些主题也添加进来。
5. 对照[随堂练习的参考答案] (`lesson1/l_glossorg.ditamap`)，自行批改一下你刚刚完成的练习作业。

## 课后练习

1. 打开文件 `lesson1/exercise_files/l_glossentry_exercise_start.dita` 和 `l_glossorg_exercise_start.dita`，使用该文件将以下内容转换成 DITA：

    --8<-- "div_exercise_content.md:start"

    <h2 style="margin: .64em 0 .64em;">关于内容策略的术语</h2>

    **结构化写作**

    一种创建内容的编辑环境。在该编辑环境中，编辑软件会强制应用某种内容结构和模板。

    **结构化内容**

    按照既定方式组织在一起的可预测信息。

    **可搜索的内容**

    可通过互联网搜索到的信息。

    **易查找的内容**

    在搜索引擎中搜索相关关键词就能查找到的信息。

    **易发现的内容**

    拥有内链的信息，尤其是在社交媒体上。

    --8<-- "div_exercise_content.md:end"

2. 对照[课后练习的参考答案] (`lesson1/exercise_files/l_glossentry_exercise_*.dita` 和 `l_glossorg_exercise.ditamap`)，自行批改一下你刚刚完成的练习作业。

<!-- links -->
[随堂练习的参考答案]: sa_glossentry.md#_2
[课后练习的参考答案]: sa_glossentry.md#_3