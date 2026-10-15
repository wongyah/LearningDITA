# 高级设置

<!-- 
    本文件隶属于在 GitHub 上开源的 DITA 培训项目。
    使用许可和版权声明，请参见 LICENSE 文件和 docs/notice.md 文件。
-->

## `collection-type` 属性

DITA 规范中规定，在关系表中，如果一个单元格中包含多个 `<topicref>` 元素，发布程序不会在这些元素引用的主题之间创建相关链接。但如果该单元格（即对应的 `<relcell>` 元素）设置了 `collection-type`属性且属性值是 `family`，任何一个 `<topicref>` 元素引用的主题都将包含指向其他主题的相关链接。

在下面的示例中，主题 A 和主题 B 中都将生成指向对方的相关链接：

```xml
<relcell collection-type="family">
	<topicref href="a.dita"/>
	<topicref href="b.dita"/>
</relcell>
```

## `linking` 属性

通常情况下，如果这两个主题（主题 A 和主题 B）位于同一行的不同列，在发布后的文档中，主题 A 中将包含指向主题 B 的相关链接，主题 B 中也将包含指向主题 A 的相关链接。

```xml
<relrow>
	<relcell>
		<topicref href="a.dita"/>
	</relcell>
	<relcell>
		<topicref href="b.dita"/>
	</relcell>
</relrow>
```

但有时候，你可能不需要或者不希望生成这些相关链接。

假如主题 B 是一个普通的任务型主题或者一个术语词条，很多概念型主题都会涉及到它，包括主题 A。你需要在主题 A（或其他概念型主题）中生成指向主题 B 的相关链接，但不希望在主题 B 中生成指向主题 A（或其他概念型主题）的相关链接。这时候，你可以为指向主题 B 的 `<topicref>` 元素添加 `linking` 属性，并将属性值设置为 `targetonly`。

```xml
<relrow>
	<relcell>
		<topicref href="a.dita"/>
	</relcell>
	<relcell>
		<topicref href="b.dita" linking="targetonly"/>
	</relcell>
</relrow>
```

反过来，假如主题 A 是某个帮助系统的“落地页”。你希望将主题 A 作为进入其他主题的入口页面，但不希望在任何地方出现指向主题 A 的链接（不管什么原因）。这时候，你可以为指向主题 A 的 `<topicref>` 元素添加 `linking` 属性，并将属性值设置为 `sourceonly`。

```xml
<relrow>
	<relcell>
		<topicref href="a.dita" linking="sourceonly"/>
	</relcell>
	<relcell>
		<topicref href="b.dita"/>
	</relcell>
</relrow>
```

## 列标题

发布文档时，DITA-OT 可以根据 `<relcolspec>` 元素中的主题类型为相关链接创建分组（分组的标题通常是“概念”、“任务”和“参考信息”）。其他发布程序也可以遵循同样的做法。在 `<relcolspec>` 元素中，你可以使用 `<title>` 元素覆盖上述分组标题。

```xml
<relcolspec type="task">
	<title>相关任务</title>
</relcolspec>
```

`<relcolspec>` 元素中也可以包含 `<topicref>` 元素。你可以使用 `<topicref>` 元素引用某个主题，为关系表列提供更多信息。如果你想深入了解 `<relcolspec>` 元素，请参见[《OASIS DITA 1.3 规范》：`<relcolspec>` 元素](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/base/relcolspec.html#relcolspec)

## 链接外部资源

在关系表中，也可以包含指向外部资源的链接。只是，`<relcolspec>` 元素和 `<relcell>` 元素中的内容会略有不同。

在下面的关系表中，第四列包含的是指向外部资源的链接。

|  概念型主题  |  任务型主题  |  参考型主题  |  网页链接  |
|:---|:---|:---|:---|
|  📄c_nourishment.dita  |  📄t_feeding.dita  |  📄r_food.dita <br/> 📄r_feeders.dita  |  📄http://www.example.com <br/> scope="external" format="html" <br/> 导航标题：鸭粮来源  |

该列的 `<relcolspec>` 元素没有设置 `type` 属性，因为里面没有 DITA 资源。不过，它用了一个 `<title>` 元素来定义该列的用途。

```xml
<relcolspec>
	<title>网页链接</title>
</relcolspec>
```

在 `<topicref>` 元素中，`href`属性的属性值是目标地址（URL），`scope`属性的属性值是 `externative`，`format`属性的属性值是 `html`。此外，`<topicref>` 元素中还包含一个 `<navtitle>` 元素，使该链接对用户更加友好：

```xml
<relcell>
	<topicref href="https://www.example.com" scope="external" format="html">
		<topicmeta>
			<navtitle>鸭粮来源</navtitle>
		</topicmeta>
	</topicref>
</relcell>
```
