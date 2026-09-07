# 插入导图引用

`<mapref>` 元素的结构如下：

```xml
<mapref href="filepath/filename.ditamap">
```

你可以使用 `href` 属性设置指向某个导图的链接。对于 `<mapref>` 元素，`format` 属性的默认属性值是 `ditamap`。上面的代码相当于：

```xml
<topicref href="filepath/filename.ditamap" format="ditamap">
```

`<mapref>` 元素中只能包含 `<topicmeta>`、`<data>` 和 `<data-about>` 这三个元数据元素。在 `<mapref>` 元素中，不允许插入 `<topicref>` 或 `<mapref>` 作为子元素。

在多张导图中复用一个主题，使用 `<topicref>` 元素；在多张导图中复用一组主题，使用 `<mapref>` 元素。使用导图引用，你就不需要在各个导图中使用 `<topicref>` 为一组主题重复创建层级结构了。

除了内容复用，`<mapref>` 元素还可以让文档发布更灵活。只要将相关导图放进一张总导图中，就可以为整个产品系列快速交付文档。`<mapref>` 元素还可以为导图添加术语表，详见随堂练习。

!!! note "注意"
    如果你想深入了解 `<mapref>` 元素，请参见 《OASIS DITA 1.3 规范》中的[`<glossgroup>` 元素](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/base/mapref.html#mapref)。

## 随堂练习

1. 打开上一节使用的练习文件 `maps_bookmaps_samples/samples/_m_ducks_start`。

2. 在最后一个 `<topicref>` 元素的后面，插入一个 `<mapref>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
    <map id="ducks">
      <title>鸭子</title>
      ...
      </topicref>
      <mapref href="g_duck_glossorg.ditamap" format="ditamap"/>
    </map>
    ```

    `<mapref>` 元素创建了一个指向术语表 `g_duck_glossorg. ditamap` 的链接。这样，你就不用在导图中使用 `<topicref>` 元素创建术语表了，那会很麻烦的！你还可以在其他导图中复用这张术语表，而且很方便。

3. 对照[随堂练习的参考答案] (`samples/_m_ducks.ditamap`)，自行批改一下你刚刚完成的练习作业 (`samples/_m_ducks_start.ditamap`)。

## 课后练习

1. 打开文件 `maps_bookmaps_samples/exercises/_m_cs101_start.ditamap`，使用该文件和主题文件们制作一张 DITA 导图。导图的层级结构如下（仅供参考）：

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

2. 对照[课后练习的参考答案] (`exercises/_m_cs101.ditamap`)，自行批改一下你刚刚完成的练习作业 (`exercises/_m_cs101_start.ditamap`)。

<!-- links -->
[随堂练习的参考答案]: sa_maps.md#_2
[课后练习的参考答案]: sa_maps.md#_3
