# 插入图片

你可以使用`<image>`元素在概念型主题中插入图片。`<image>`元素使用`href`属性创建一个指向本地图片或网络图片的链接。

和`<p>`元素一样，`<image>`元素也可以用在`<conbody>`元素中的任何位置。它也经常作为行内图片放在`<p>`元素里。

你可以使用`<fig>`元素插入带有标题的图片。一个`<fig>`元素中可以有一个`<title>`元素、一个或多个`<image>`元素。

## 随堂练习

1. 为文件`lesson2/l_concept_images_tables_start.dita`创建一个副本，然后在编辑器中打开。

    你看到的文件内容应该是这样的：

    ```xml
    --8<-- "sample_files/concept_topic/lesson2/l_concept_images_tables_start.dita"
    ```

2. 在`<conbody>`元素中，插入一个`<image>`元素如下（代码示例插入的图片为`lesson2/images/ducklings_swimming.jpg`，来源于 Flickr, Micolo J.）：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_images_tables">
      <title>小鸭子的生长发育</title>
      <conbody>
        <image href="images/ducklings_swimming.jpg"/>
      </conbody>
    </concept>
    ```

    在刚刚插入的`<image>`元素中，有一个指向图片所在位置的链接（`href`）。`<image>`元素中的链接可以指向服务器上的图片路径，也可以指向网络图片的网址。

3. 在`<image>`元素的后面，插入一个`<fig>`元素如下（代码示例插入的图片为`lesson2/images/ducklings_running.jpg`，来源于 Airwolfhound @Flickr）：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_images_tables">
      <title>小鸭子的生长发育</title>
      <conbody>
        ...
        <fig>
          <title>奔跑的小鸭子</title>
          <image href="images/ducklings_running.jpg"/>
        </fig>
      </conbody>
    </concept>
    ```

    在概念型主题中还有一种插入图片的方法：使用`<fig>`元素。

    在刚刚插入的`<fig>`元素中，有一个`<title>`元素和一个`<image>`元素。`<title>`元素可以为图片添加标题。

    `<image>`元素在`<fig>`元素中的使用方式和在`<conbody>`元素中一模一样。

    一个`<fig>` 元素中可以有一个或多个`<image>`元素（但只能有一个`<title>`元素）。

    !!! note "注意"
        在`<fig>`元素中，`<title>`元素必须位于`<image>`元素的前面。但是在最终发布的文档中，图片标题既可以位于图片的上方，也可以位于图片的下方。
