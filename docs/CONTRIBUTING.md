#  Contributing Guide | 贡献指南 

[English](#contributing-guide) | [中文](#贡献指南)


## Contributing Guide

Thank you for your interest in the DesignPicker localization project! This document will guide you on how to contribute translations, ensuring quality and consistency.

### Before You Start

1. **Familiarize yourself with DesignPicker**: If possible, install and use the DesignPicker extension to understand its features and interface.
2. **Review existing translations**: Browse through existing language translations to understand the style and terminology usage.
3. **Read the terminology guide**: Check the [Terminology Guide](TERMS.md) to ensure consistency in terminology.

### Translation File Format

DesignPicker uses JSON format for localization files. Each language has a `messages.json` file located in the `_locales/[language_code]/` directory.

Example file structure:

```json
{
  "appName": {
    "message": "DesignPicker"
  },
  "appDesc": {
    "message": "A smart color picker and font detection tool"
  },
  "colors": {
    "message": "Colors"
  }
}
```

### Translation Steps

1. **Choose a language**:
   - If you're updating an existing language, find the corresponding `_locales/[language_code]/messages.json` file
   - If adding a new language, create a new language directory and file

2. **Translate content**:
   - Only translate the value of the `"message"` field
   - Do not modify the key names (like `"appName"`)
   - Keep placeholders (like `$1`, `$format$`) intact

3. **Handle placeholders**:
   - Some strings contain placeholders like `$1`, `$format$`, etc.
   - These placeholders will be replaced with actual values at runtime
   - Make sure to keep these placeholders in your translation and place them appropriately according to the grammar rules of the target language

   For example:
   ```json
   "switchToFormat": {
     "message": "Switch to $format$",
     "placeholders": {
       "format": {
         "content": "$1"
       }
     }
   }
   ```

   Spanish translation:
   ```json
   "switchToFormat": {
     "message": "Cambiar a $format$",
     "placeholders": {
       "format": {
         "content": "$1"
       }
     }
   }
   ```

4. **Test your translation**:
   - If possible, test your translation locally
   - Ensure UI elements display correctly without text overflow or truncation

### Translation Quality Guidelines

1. **Stay professional**:
   - Use formal, professional language
   - Avoid slang, internet jargon, or overly colloquial expressions

2. **Respect the original meaning**:
   - Ensure your translation accurately conveys the meaning of the original text
   - Don't add or remove information

3. **Localize, don't just translate**:
   - Aim for natural, fluent expressions rather than word-for-word translations
   - Consider the idiomatic expressions and cultural context of the target language

4. **Maintain consistency**:
   - The same term should be translated consistently throughout
   - Refer to the terminology guide and existing translations

5. **Mind the formatting**:
   - Maintain proper punctuation
   - Pay attention to spacing (some languages like Chinese typically don't use spaces before or after punctuation)

### Submitting Your Translation

1. **Create a branch**:
   ```bash
   git checkout -b translate-[language_code]
   ```

2. **Commit your changes**:
   ```bash
   git add .
   git commit -m "Add/Update [Language Name] translation"
   git push origin translate-[language_code]
   ```

3. **Create a Pull Request**:
   - Create a PR on GitHub
   - Provide a brief description of your changes
   - Add any special instructions or notes if necessary

### Language Code Reference

Here are some common language codes:

- English: `en`
- Simplified Chinese: `zh_CN`
- Traditional Chinese: `zh_TW`
- French: `fr`
- German: `de`
- Spanish: `es`
- Japanese: `ja`
- Korean: `ko`
- Russian: `ru`
- Portuguese: `pt`
- Italian: `it`
- Dutch: `nl`
- Polish: `pl`
- Turkish: `tr`
- Vietnamese: `vi`
- Czech: `cs`
- Danish: `da`
- Indonesian: `id`
- Romanian: `ro`
- Swedish: `sv`
- Hungarian: `hu`

### Issues and Help

If you encounter any issues or need help during the translation process, please:

- Create an Issue on GitHub
- Add comments to your PR
- Contact the project maintainers

Thank you again for contributing to the localization of DesignPicker!


---


## 贡献指南

感谢您对 DesignPicker 本地化项目的关注！本文档将指导您如何为项目贡献翻译，确保翻译质量和一致性。

### 开始之前

1. **熟悉 DesignPicker**：如果可能，请先安装并使用 DesignPicker 扩展，了解其功能和界面。
2. **查看现有翻译**：浏览已有的语言翻译，了解翻译风格和术语使用。
3. **阅读术语表**：查看 [术语表](TERMS.md) 以确保术语一致性。

### 翻译文件格式

DesignPicker 使用 JSON 格式的本地化文件。每种语言都有一个 `messages.json` 文件，位于 `_locales/[语言代码]/` 目录下。

文件结构示例：

```json
{
  "appName": {
    "message": "DesignPicker"
  },
  "appDesc": {
    "message": "A smart color picker and font detection tool"
  },
  "colors": {
    "message": "Colors"
  }
}
```

### 翻译步骤

1. **选择语言**：
   - 如果您要更新现有语言，找到对应的 `_locales/[语言代码]/messages.json` 文件
   - 如果要添加新语言，创建新的语言目录和文件

2. **翻译内容**：
   - 只翻译 `"message"` 字段的值
   - 不要修改键名（如 `"appName"`）
   - 保留占位符（如 `$1`、`$format$`）不变

3. **处理占位符**：
   - 某些字符串包含占位符，如 `$1`、`$format$` 等
   - 这些占位符会在运行时被实际值替换
   - 请确保在翻译中保留这些占位符，并根据目标语言的语法规则放置在适当位置

   例如：
   ```json
   "switchToFormat": {
     "message": "Switch to $format$",
     "placeholders": {
       "format": {
         "content": "$1"
       }
     }
   }
   ```

   中文翻译：
   ```json
   "switchToFormat": {
     "message": "切换到 $format$",
     "placeholders": {
       "format": {
         "content": "$1"
       }
     }
   }
   ```

4. **测试翻译**：
   - 如果可能，请在本地测试您的翻译
   - 确保界面元素显示正确，没有文本溢出或截断

### 翻译质量指南

1. **保持专业**：
   - 使用正式、专业的语言
   - 避免俚语、网络用语或过于口语化的表达

2. **尊重原意**：
   - 确保翻译准确传达原文的含义
   - 不要添加或删除信息

3. **本地化而非直译**：
   - 追求自然流畅的表达，而非逐字翻译
   - 考虑目标语言的习惯用法和文化背景

4. **保持一致性**：
   - 同一术语在整个翻译中应保持一致
   - 参考术语表和已有翻译

5. **注意格式**：
   - 保持标点符号的正确使用
   - 注意空格的使用（某些语言如中文通常不在标点前后使用空格）

### 提交翻译

1. **创建分支**：
   ```bash
   git checkout -b translate-[语言代码]
   ```

2. **提交更改**：
   ```bash
   git add .
   git commit -m "Add/Update [语言名称] translation"
   git push origin translate-[语言代码]
   ```

3. **创建 Pull Request**：
   - 在 GitHub 上创建 PR
   - 提供简要说明，描述您所做的更改
   - 如有必要，添加任何特殊说明或注释

### 语言代码参考

以下是一些常见语言的代码：

- 英语: `en`
- 简体中文: `zh_CN`
- 繁体中文: `zh_TW`
- 法语: `fr`
- 德语: `de`
- 西班牙语: `es`
- 日语: `ja`
- 韩语: `ko`
- 俄语: `ru`
- 葡萄牙语: `pt`
- 意大利语: `it`
- 荷兰语: `nl`
- 波兰语: `pl`
- 土耳其语: `tr`
- 越南语: `vi`
- 捷克语: `cs`
- 丹麦语: `da`
- 印尼语: `id`
- 罗马尼亚语: `ro`
- 瑞典语: `sv`
- 匈牙利语: `hu`

### 问题和帮助

如果您在翻译过程中遇到任何问题或需要帮助，请：

- 在 GitHub 上创建 Issue
- 在 PR 中添加评论
- 联系项目维护者

再次感谢您对 DesignPicker 本地化的贡献！

---