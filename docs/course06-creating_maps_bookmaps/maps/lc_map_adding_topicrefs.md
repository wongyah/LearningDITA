# 插入主题引用

`<topicref>` 元素的结构如下：

```xml
<topicref href="filepath/filename.dita">
```

你可以使用 `href` 属性设置指向某个主题的链接。在 DITA 中，`<topicref>` 元素只能引用导图所在文件夹及其子文件夹里的主题。否则，文档发布时可能会出错。因此，最好将导图保存在根目录或顶层文件夹中。

主题引用元素（`<topicref>`）中可以包含以下元素：

- `<topicmeta>` 元素，可以在导图中为主题添加元数据。
- 任意数量的 `<topicref>` 元素。
- 任意数量的 `<mapref>` 元素。

你可以创建具有层级结构的导图，只要在 `<topicref>` 元素中嵌套 `<topicref>` 或 `<mapref>` 元素即可。这样，也便于将主题们组织在一起。将导图发布成文档时，文档目录取决于导图的层级结构。

嵌套 `<topicref>` 元素时，始终要想着最终要发布的文档应该是什么样的。在 DITA 中，`<topicref>` 元素中允许嵌套任意数量的 `<topicref>` 元素，没有上限。每嵌套一层 `<topicref>` 元素，相当于在发布后的文档中新增一级标题。按照最佳实践，`<topicref>` 元素的嵌套层级不要超过五层（2~3 层最为理想）。

<!-- [视频：创建 DITA 导图](https://youtu.be/3rDlOvDguiw) -->

!!! note "注意"
    如果你想深入了解 `<topicref>` 元素，请参见 《OASIS DITA 1.3 规范》中的[`<topicref>` 元素](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/base/topicref.html#topicref)。

## 随堂练习

1. 打开上一节使用的练习文件 `maps_bookmaps_samples/samples/_m_ducks_start`。

2. 在 `<title>` 元素的后面，插入一个 `<topicref>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
    <map id="ducks">
      <title>鸭子</title>
      <topicref href="c_wild_ducks.dita">
      </topicref>
    </map>
    ```

    该 `<topicref>` 元素创建了一个指向概念型主题 `c_wild_ducks.dita` 的链接。

3. 在你刚刚插入的 `<topicref>` 元素中，再插入一个 `<topicref>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
    <map id="ducks">
      <title>鸭子</title>
      <topicref href="c_wild_ducks.dita">
        <topicref href="c_wild_duck_types.dita"/>
      </topicref>
    </map>
    ```

    将第二个 `<topicref>` 元素嵌套在第一个 `<topicref>` 元素中，意味着在该导图中 `c_wild_duck_types.dita` 是 `c_wild_duck.dita` 的子主题。

4. 在刚刚插入的 `<topicref>` 元素的后面，再插入两个 `<topicref>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
    <map id="ducks">
      <title>鸭子</title>
      <topicref href="c_wild_ducks.dita">
        <topicref href="c_wild_duck_types.dita"/>
        <topicref href="c_wild_duck_species.dita"/>
        <topicref href="t_watching_wild_ducks.dita"/>
      </topicref>
    </map>
    ```

    有了新插入的 `<topicref>` 元素，DITA 导图的层级结构变得更清晰了。`c_wild_duck_types.dita`、`c_wild_duck_species.dita` 和 `t_watching_wild_ducks.dita` 都是关于野鸭的主题，所以一起放在 `c_wild_ducks. dita` 主题下。

5. 在指向 `c_wild_ducks.dita` 主题的 `<topicref>` 元素后面，再插入两个 `<topicref>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
    <map id="ducks">
      <title>鸭子</title>
      <topicref href="c_wild_ducks.dita">
        <topicref href="c_wild_duck_types.dita"/>
        <topicref href="c_wild_duck_species.dita"/>
        <topicref href="t_watching_wild_ducks.dita"/>
      </topicref>
      <topicref href="c_domestic_ducks.dita">
        <topicref href="c_duckling_growth.dita"/>
        <topicref href="c_feeding_ducklings.dita">
          <topicref href="c_duck_weight.dita"/>
        </topicref>
      </topicref>
      <topicref href="c_duckdb.dita">
        <topicref href="c_writing_about_ducks.dita" locktitle="yes"/>
        <topicref href="r_tnav.dita"/>
      </topicref></map>
    ```

    现在，这张导图中有了三个一级主题（`<topicref>`）：`c_wild_ducks.dita`、`c_domestic_ducks.dita` 和 `c_duckdb. dita`。每个一级主题中都有几个二级主题。其中一个二级主题 `c_feeding_ducklings.dita` 中，还有一个三级主题 `c_duck_weight.dita`。
