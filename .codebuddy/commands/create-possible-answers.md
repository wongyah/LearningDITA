【任务说明】

请以 ${spec_file: -docs/course03-authoring_tasks/task_intro/sa_new_task.md} 为模板，在 ${target_folder} 文件夹中创建一个新文件。

在新文件中，使用 ${snippet_folder} 中的文件替换模板文件里对应的 XML 代码。同时，根据 ${snippet_folder} 中的文件名称命名新文件。

假设 ${snippet_folder} 文件夹中有三个文件：`l_topic_name.dita`、`l_topic_name_start` 和 `l_topic_name_exercise.dita`。
你应该在新文件中使用 `${snippet_folder}/l_topic_name.dita` 替换模板文件中的 `sample_files/task_topic/lesson1/l_new_task.dita`，使用 `${snippet_folder}/l_topic_name_exercise.dita` 替换模板文件中的 `sample_files/task_topic/lesson1/l_new_task_exercise.dita`。同时，将新文件命名为 `sa_topic_name.md`。

使用 ${course_demo} 文件的文件名替换链接 `[随堂练习]` 的目标文件，使用 ${exercise} 文件的文件名替换链接 `[课后练习]` 的目标文件。

【本次任务变量】

- target_folder: ${target_folder}
- snippet_folder: ${snippet_folder}
- course_demo: ${course_demo}
- exercise: ${exercise}