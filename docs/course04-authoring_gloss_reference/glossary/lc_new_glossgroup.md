# 新建术语分组主题

一个最简单的术语分组主题，至少要包含一个根元素 `<glossgroup>`（带 `id` 属性）。`<glossgroup>`元素中至少要包含一个 `<title>` 元素、一个或以上 `<glossentry>` 或 `<glossgroup>` 元素（带 `id` 属性）。

!!! note "注意"
    本讲的主要内容是术语分组主题中元素的基本用法。如果你想了解每个元素的详细用法，请参见 [《OASIS DITA 1.3 规范》：`<glossgroup>`](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/technicalContent/glossgroup.html#glossgroup)。

<!-- [视频：创建术语分组主题](https://youtu.be/csP8WUT7EEs) -->

## 随堂练习

1. 为文件 `l_glossgroup_start.dita` 创建一个副本，然后在编辑器中打开。

    !!! note "注意"
        如果你使用的是支持DITA的编辑器，请使用文本模式，不要使用写作模式或者其他可视模式。

    你看到的文件内容应该是这样的：

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <!DOCTYPE glossgroup PUBLIC "-//OASIS//DTD DITA Glossary Group//EN" "glossgroup.dtd">
    <glossgroup id="duck_equipment">
     <title></title>
    </glossgroup>
    ```

    - 第一行（以 `<?xml` 开头）是XML声明。XML声明是XML文件的一个标准组成部分。
    - 第二行是文档类型声明（即DOCTYPE声明），用来声明该文件是一个术语分组主题。对主题内容进行验证时，程序会用到该信息。每个主题类型的文档类型（即DOCTYPE）都各不相同，包括通用任务主题。
    - 第三行是 `<glossgroup>` 元素的开始标签。`id` 属性是 `<glossgroup>` 元素的必选属性。
    - 第四行是 `<title>` 元素。

2. 在 `<title>` 元素中，为术语分组输入一个标题如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE glossgroup PUBLIC "-//OASIS//DTD DITA Glossary Group//EN" "glossgroup.dtd">
    <glossgroup id="duck_equipment">
     <title>观鸭设备</title>
    </glossgroup>
    ```

    根据术语分组主题的文档结构定义，`<title>` 元素是必选元素，但 `<title>` 元素的内容可以为空。

3. 在 `<title>` 元素的后面，插入四个 `<glossentry>` 元素，每个 `<glossentry>` 元素都要有一个 `id` 属性。

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE glossgroup PUBLIC "-//OASIS//DTD DITA Glossary Group//EN" "glossgroup.dtd">
    <glossgroup id="duck_equipment">
     <title>观鸭设备</title>
     <glossentry id=""></glossentry>
     <glossentry id=""></glossentry>
     <glossentry id=""></glossentry>
     <glossentry id=""></glossentry>
    </glossgroup>
    ```

4. 在每个 `<glossentry>` 元素中，都插入一个 `<glossterm>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE glossgroup PUBLIC "-//OASIS//DTD DITA Glossary Group//EN" "glossgroup.dtd">
    <glossgroup id="duck_equipment">
     <title>观鸭设备</title>
    <glossentry id="binoculars">
     <glossterm>双筒望远镜</glossterm>
    </glossentry>
    <glossentry id="duck_bait">
     <glossterm>鸭饲料</glossterm>
    </glossentry>
    <glossentry id="duck_call">
     <glossterm>仿生鸭哨</glossterm>
    </glossentry>
    <glossentry id="spotting_scope">
     <glossterm>鉴识望远镜</glossterm>
    </glossentry>
    </glossgroup>
    ```

5. 在每个 `<glossterm>` 元素的后面，都插入一个 `<glossdef>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE glossgroup PUBLIC "-//OASIS//DTD DITA Glossary Group//EN" "glossgroup.dtd">
    <glossgroup id="duck_equipment">
     <title>观鸭设备</title>
    <glossentry id="binoculars">
     <glossterm>双筒望远镜</glossterm>
     <glossdef>一种用双眼观察远处物体的光学设备。</glossdef>
    </glossentry>
    <glossentry id="duck_bait">
     <glossterm>鸭饲料</glossterm>
     <glossdef>吸引鸭子的饲料，涵盖从颗粒饲料到廉价的白面包等。</glossdef>
    </glossentry>
    <glossentry id="duck_call">
     <glossterm>仿生鸭哨</glossterm>
     <glossdef>一根装有芦苇的管子，可以模仿鸭子的叫声。</glossdef>
    </glossentry>
    <glossentry id="spotting_scope">
     <glossterm>鉴识望远镜</glossterm>
     <glossdef>一种用单眼观察远处物体的光学设备，可以比双筒望远镜看到更多细节。</glossdef>
    </glossentry>
    </glossgroup>
    ```
