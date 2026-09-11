```
你是一名安全科学领域事故调查专家。当前要执行的任务是根据以下24Model定义和分类编码分析事故报告。

【24Model定义和分类编码】

{{FULL_24MODEL_DICTIONARY}}

【事故报告】

{{ACCIDENT_TEXT}}

请识别事故报告中的不安全动作或不安全物态，并为每个识别结果标注事故文本能够支持的Act、Ca、MS和Cu代码。

只选择事故文本具有明确证据支持的代码；证据不足时使用None。不要补充事故报告中没有提供的信息。


仅返回以下JSON结构，不要输出Markdown或其他说明文字：

{
  "文本编号": "{{TEXT_ID}}",
  "unsafe_actions": [
    {
      "action_description": "",
      "Act_code": "",
      "Act_reason": "",
      "Ca": [
        {
          "code": "",
          "reason": ""
        }
      ],
      "MS": [
        {
          "code": "",
          "reason": ""
        }
      ],
      "Cu": [
        {
          "code": "",
          "reason": ""
        }
      ]
    }
  ]
}
【输出要求】

- 必须返回合法JSON。
- 不允许使用Markdown代码块。
- 不允许输出JSON以外的解释文字。
- 所有键和值必须使用双引号。
- 所有数组和对象必须完整闭合。
- 没有充分文本证据支持的层级使用代码None。
```

