# 在书籍导图中插入术语表

<!-- 
    本文件隶属于在 GitHub 上开源的 DITA 培训项目。
    使用许可和版权声明，请参见 LICENSE 文件和 docs/notice.md 文件。
-->

如果使用书籍导图组织 DITA 主题，请在 `<frontmatter>` 或 `<backmatter>` 元素中插入一个 `<booklists>` 元素，再在 `<booklists>` 元素中插入一个 `<glossarylist>` 元素。`<glossarylist>` 元素可以让发布程序知道应该在什么位置插入术语表。

```xml
<booklists>
 ...
 <glossarylist>
  <topicref href="glossary.ditamap" format="ditamap"/>
 </glossarylist>
 ...
</booklists>
```

如果要引用术语导图，推荐使用 `<topicref>` 元素，如上例所示。
