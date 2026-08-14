【任务说明】

请参照 ${spec_file:-docs/course03-authoring_tasks/task_intro/lc_creating_new.md} 中的规范，将源文件 ${source_file} 转换成 Markdown 格式格式，并保存到目标路径 ${target_path} 中的同名文件中。

注意：只做格式转换，不要擅自修改任何内容。

【默认目标路径】

如果没有指定 ${target_path}，请将文件保存到 `docs` 文件下的同名文件夹中，例如：

源文件 ${source_file} 为：
`DITA-1.3/zh-cn/course04-authoring_gloss_reference/reference/lc_adding_properties.dita`

目标文件应该为：
`docs/course04-authoring_gloss_reference/reference/lc_adding_properties.md`


【本次任务变量】

- source_file: ${source_file}
- target_path: ${target_path}
- spec_file: (可选) 默认为 docs/course03-authoring_tasks/task_intro/lc_creating_new.md
