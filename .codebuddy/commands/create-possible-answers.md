# 生成参考答案页

## 任务说明

请以 ${spec_file: -docs/course03-authoring_tasks/task_intro/sa_new_task.md} 为模板，在 ${target_folder} 文件夹中创建一个新文件。

### 替换 XML 代码

在新文件中，使用 ${snippet_folder} 中的文件替换模板文件里对应的 XML 代码。同时，根据 ${snippet_folder} 中的文件名称命名新文件。

假设 ${snippet_folder} 文件夹中有三个文件：`l_topic_name.dita`、`l_topic_name_start` 和 `l_topic_name_exercise.dita`。
你应该在新文件中使用 `${snippet_folder}/l_topic_name.dita` 替换模板文件中的 `sample_files/task_topic/lesson1/l_new_task.dita`，使用 `${snippet_folder}/l_topic_name_exercise.dita` 替换模板文件中的 `sample_files/task_topic/lesson1/l_new_task_exercise.dita`。同时，将新文件命名为 `sa_topic_name.md`。

## 更新链接

将链接 `[随堂练习]` 的目标文件替换为本讲中的第一节含有随堂练习的课程文件的文件名。该文件里随堂练习的第一步通常包含以下文本：“为文件 `filename` 创建一个副本，然后在编辑器中打开”。

将链接 `[课后练习]` 的目标文件替换为本讲中含有课后练习的课程文件的文件名（${last_file}）。

## 检查作业批改步骤

请参考文件 docs/course03-authoring_tasks/task_intro/lc_optional_elements.md，检查 ${last_file} 中的随堂练习和课后练习是否包含自行批改练习作用的说明步骤（通常为练习的最后一步。

如果缺少该步骤，请按照参考文件中的模式添加上。

## 修改课后练习的内容格式

将 ${last_file} 中课后练习的内容格式从 HTML 修改为 Markdown，模式如下：

```
    --8<-- "div_exercise_content.md:start"
    <h2 style="margin: .64em 0 .64em;">如果有标题</h2>

    Markdown 格式的内容

    --8<-- "div_exercise_content.md:end"    
```

如果 ${snippet_folder} 中有 `*_exercise.dita` 文件，请使用该文件中的中文内容将英文内容替换掉。如果没有，请你翻译将英文内容翻译成中文。

## 本次任务变量

- target_folder: ${target_folder}
- snippet_folder: ${snippet_folder}
- last_file: ${last_file}
