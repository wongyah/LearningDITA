# 插入更多高级元素

下面是DITA中常见的另一些高级元素：

| 元素 | 说明 |
|---|---|
| `<section>` | 将主题的正文划分为多个小节，每个小节都有独立的标题。一个`<section>`元素中可以有一个`<title>`元素和大多数`<conbody>`元素中可以使用的元素。不过，`<section>`元素不允许自嵌套。`<section>`元素的后面只能接`<section>`元素、`<example>`元素或者`<conbodydiv>`元素。 |
| `<draft-comment>` | 在内容中插入批注。在默认情况下，`<draft-comment>`元素不会显示在发布后文档中。因此，发布文档时不需要删除批注。（但你得权衡一下是否有必要冒险！） |
| `<required-cleanup>` | 标记因用错了元素标签而需要修改的内容。在默认情况下，`<required-cleanup>`元素中的内容不会显示在发布后文档中。 |

## 随堂练习

1. 请继续使用文件 `lesson4/l_concept_advanced_start.dita` 进行练习，在里面插入上面提到的元素。

2. 在 `<lq>` 元素的后面，插入一个 `<section>` 元素如下：

    在本例中，你在“描写鸭子”的主题中新增了一个小节。

3. 在 `<section>` 元素中，插入一个 `<title>` 元素和一个 `<p>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_advanced">
     <title>描写鸭子</title>
     <conbody>
      ...
      <section>
       <title>分享鸭子数据库</title>
       <p>将鸭子数据库导出为HTML文件，以便在网站上分享。你还可以为数据库添加一个下载链接，让用户自行下载。</p>
      </section>
     </conbody>
    </concept>
    ```

    在 `<concept>` 元素中，有且只能有一个标题（`<title>`）。但通过使用 `<section>` 元素，你可以在概念型主题中添加多个子标题。和 `<concept>` 元素一样，在 `<section>` 元素中也是有且只能有一个标题（`<title>`）。

    `<section>` 元素中允许插入的元素和 `<conbody>` 一模一样，只有一个元素例外：`<section>`。`<section>` 不允许自嵌套，也就是说，你不能在一个 `<section>` 元素中插入另一个 `<section>` 元素。

4. 在新小节中的 `<p>` 元素后面，插入一个 `<draft-comment>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_advanced">
     <title>描写鸭子</title>
     <conbody>
      ...
      </p>
      <draft-comment>你确定要提供下载渠道吗？</draft-comment>
      ...
     </conbody>
    </concept>
    ```

    在本例中，你通过批注与参与编辑这个主题的其他写作人员沟通，希望他们重新考虑一下是否真要提供下载渠道。

5. 在新小节的末尾（`<section>` 元素的结束标签之前），插入一个 `<required-cleanup>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_advanced">
     <title>描写鸭子</title>
     <conbody>
      ...
      <required-cleanup>
       <p>请考虑一下是否可以为用户提供一个提交反馈或者提供鸭子种类等建议的渠道。</p>
      </required-cleanup>
      </section>
     </conbody>
    </concept>
    ```

    在本例中，你通过 `<required-cleanup>` 元素进行沟通，提醒写作人员必须将元素中的内容移动到一个合法的位置（比如 `<section>` 元素中）或者更换成一个合法的元素（比如 `<example>` 元素）。否则，由于存在非法元素，该主题就无法发布成文档。

6. 对照随堂练习的参考答案 `l_concept_advanced.dita`，自行批改一下你刚刚完成的练习作业 `lesson4/l_concept_advanced_start.dita`。

## 课后练习

1. 打开文件 `lesson4/l_concept_advanced_exercise_start.dita`，使用该文件将以下内容转换成DITA：

    --8<-- "sample_content.md:start"

    <h2 style="margin: .64em 0 .64em;">制定技术内容策略</h2>

    完成对现有信息产品的评估之后，你应该就可以整理出一份有关内容的问题清单和改善建议。下面是一些常见的场景。

    <h3>技术文档与培训材料之间的内容复用</h3>

    培训部门会使用技术文档团队创建的参考信息和操作指南。但课程设计师只能通过复制粘贴来使用这些内容，不能直接复用内容或者插入链接，因为两个团队使用的是不同内容创作工具，而且互不兼容。

    > **批注**
    > 建议补充："如果统一使用同一套工作流程，两个团队之间就可以无缝共享内容，减少大量枯燥的重复性工作。”
    {: style="margin: 1.5em 0;"}

    <h3>除了PDF，还需要发布HTML</h3>

    你的内容在HTML中看起来可能是这样的：

    ```html
     <div class="p">你可以产出价值高的内容，例如以下几类：
      <ul class="ul">
       <li class="li"><p> class="p">培训材料</p></li>
       <li class="li"><p> class="p">白皮书</p></li>
       <li class="li"><p> class="p">知识库文章</p></li>
      </ul>
     </div>
    ```

    其中，`<div>`元素中包含了一个无序列表。

    <h3>内容与目标受众不匹配</h3>
    
    *内容针对的是错误的受众。例如，医院写给患者的一份文档，使用的全是只有医学界的专业人士才能看懂的复杂的医学术语。*

    --8<-- "sample_content.md:end"

2. 对照课后练习的参考答案 `lesson4/l_concept_advanced_exercise.dita`，自行批改一下你刚刚完成的练习作业 `lesson4/l_concept_advanced_exercise_start.dita`。
