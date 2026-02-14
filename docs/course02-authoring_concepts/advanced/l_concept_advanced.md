# 参考答案

## 随堂练习的参考答案

本讲中[随堂练习]的参考答案如下：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
<concept id="concept_advanced">
  <title>描写鸭子</title>
  <conbody>
    <codeblock>duckdata> add entry (绿头鸭)
;
1 entry added (0.05 sec)
duckdata> _
</codeblock>
    <p>要在数据库中添加一条关于鸭子种类的记录，请在命令行中输入<codeph>add entry</codeph>，接着在圆括号中输入鸭子的种类，然后按回车键。</p>
      <lq href="https://commons.digitalthoreau.org/walden/the-ponds/the-ponds-18-34/" format="html" scope="external">可比农夫家门前的池塘清澈多了！他家的鸭子在那个池塘游泳。一群纯洁的野鸭纷纷飞向这里。大自然的美，竟无一人懂得欣赏。鸟语花香，相映成趣。但世上的少男少女，谁又能真正懂得欣赏大自然的浑然天成和生机盎然之美?</lq>
    <section>
      <title>分享鸭子数据库</title>
      <p>将鸭子数据库导出为HTML文件，以便在网站上分享。你还可以为数据库添加一个下载链接，让用户自行下载。</p>
      <draft-comment>你确定要提供下载渠道吗？</draft-comment>
      <required-cleanup>
        <p>请考虑一下是否可以为用户提供一个提交反馈或者鸭子种类等建议的渠道。</p>
      </required-cleanup>
    </section>
  </conbody>
</concept>
```

## 课后练习的参考答案

本讲中[课后练习]的参考答案如下：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
<concept id="concept_advanced_exercise">
  <title>制定技术内容策略</title>
  <conbody>
    <p>完成对现有信息产品的评估之后，你应该就可以整理出一份有关内容的问题清单和改善建议。下面是一些常见的场景。</p>
    <section>
      <title>技术文档与培训材料之间的内容复用</title>
      <p>培训部门会使用技术文档团队创建的参考信息和操作指南。但课程设计师只能通过复制粘贴来使用这些内容，不能直接复用内容或者插入链接，因为两个团队使用的是不同内容创作工具，而且互不兼容。</p>
      <draft-comment>建议补充："如果统一使用同一套工作流程，两个团队之间就可以无缝共享内容，减少大量枯燥的重复性工作。”</draft-comment>
    </section>
    <section>
      <title>除了PDF，还需要发布HTML</title>
      <p>你的内容在HTML中看起来可能是这样的：</p>
      <codeblock>&lt;div class="p">你可以产出价值高的内容，例如以下几类：
&lt;ul class="ul">
&lt;li class="li">&lt;p class="p">培训材料&lt;/p>&lt;/li>
&lt;li class="li">&lt;p class="p">白皮书&lt;/p>&lt;/li>
&lt;li class="li">&lt;p class="p">知识库文章&lt;/p>&lt;/li>
&lt;/ul>
&lt;/div></codeblock>
      <p>其中，<codeph>&lt;div></codeph>元素中包含了一个无序列表。</p>
    </section>
    <section>
      <title>内容与目标受众不匹配</title>
      <lq href="https://www.scriptorium.com/content-transformation/" format="html" scope="external">内容针对的是错误的受众。例如，医院写给患者的一份文档，使用的全是只有医学界的专业人士才能看懂的复杂的医学术语。</lq>
    </section>
  </conbody>
</concept>
```

[随堂练习]: lc_advanced.md#_2
[课后练习]: lc_more_advanced.md#_3