# 地表水自动监测技术规范 (HJ 915-2017) - 交互式AI思维导图

本项目是一个交互式的思维导图，旨在帮助用户理解和学习《地表水自动监测技术规范 (HJ 915-2017)》。它结合了AI技术，为规范的各个章节提供智能解读、场景模拟和问答功能。

## 主要功能

*   **交互式思维导图浏览**：用户可以方便地展开和折叠规范的各个章节和条款。
*   **AI智能解读**：点击思维导图中的节点，可以获取由AI（Gemini或DeepSeek模型）生成的对该节点内容的详细解释和重要性说明。
*   **AI智能问答**：内置搜索框，用户可以就规范内容自由提问，AI将根据规范给出解答。
*   **章节测验**：部分重要章节配有小测验，帮助用户巩固学习效果。
*   **场景模拟**：针对特定操作或要求，提供AI驱动的场景模拟，帮助用户理解在实际操作中如何应用规范。
*   **AI模型选择**：用户可以选择使用 Google Gemini 或 DeepSeek 作为后端AI模型。
*   **API密钥本地存储**：用户的API密钥将安全地存储在浏览器的本地存储中，不会上传到其他任何地方。
*   **导入思维导图 (Import Mind Map)**: 用户可以导入外部的JSON文件来替换当前显示的思维导图内容。

## 如何使用

1.  **打开文件**：在现代的网页浏览器中打开 `AI思维导图.html` 文件。
2.  **选择AI模型**：在页面上方的设置区域，选择您希望使用的AI模型（Gemini 或 DeepSeek）。
3.  **配置API密钥**：
    *   输入您所选AI模型的有效API密钥。
    *   点击“保存密钥”按钮。密钥将保存在您浏览器的本地存储中，仅用于与相应的AI服务接口通信。
    *   如果需要更换或清除密钥，可以使用相应的“清除密钥”按钮。
4.  **浏览与交互**：
    *   点击思维导图节点旁的 `+` 或 `-` 图标来展开或折叠分支。
    *   点击节点文字右侧的 ✨ 图标，AI会对该章节进行智能解读。
    *   部分节点提供 🧠 图标，点击可进入AI场景模拟。
    *   部分节点解读后会提供 📝 图标，点击可开始章节测验。
    *   使用页面上方的搜索框就规范内容进行提问。
5.  **导入自定义思维导图 (Import Custom Mind Map):**
    *   在 "全部展开" / "全部折叠" 按钮附近，您会找到一个文件选择框和一个 "导入思维导图" 按钮。
    *   点击文件选择框，选择一个本地的 JSON 文件。
    *   该JSON文件应代表一个思维导图的结构。根对象应包含 `text` (字符串类型) 属性和可选的 `children` (数组类型) 属性。
    *   `children` 数组中的每个元素也应为一个对象，包含 `text` 属性和可选的 `children` 属性。
    *   示例JSON结构:
        ```json
        {
          "text": "我的自定义根节点",
          "isRoot": true, // 可选，但建议根节点使用
          "children": [
            { 
              "text": "子节点1",
              "children": [
                { "text": "孙子节点A" }
              ]
            },
            { "text": "子节点2" }
          ]
        }
        ```
    *   选择文件后，点击 "导入思维导图" 按钮。
    *   如果文件有效，当前思维导图将被替换为导入的内容。如果文件无效或格式不正确，将显示错误消息。
    *   **注意**: 导入功能会替换当前显示的思维导图。如果您想保留当前内容，请确保在导入前有其他备份。

## 注意事项

*   **API密钥**：您需要自行获取所选AI模型（Google Gemini 或 DeepSeek）的API密钥。本工具不提供API密钥。
*   **浏览器兼容性**：建议使用最新版本的Chrome、Edge、Firefox或Safari浏览器以获得最佳体验。
*   **本地存储**：API密钥存储在浏览器的Local Storage中。清除浏览器缓存或在隐私模式下使用可能会导致已保存的密钥丢失。

## 技术栈

*   HTML
*   Tailwind CSS
*   JavaScript

## 隐私声明

用户提供的API密钥仅存储在用户浏览器的本地存储中，用于与用户选择的AI服务（Gemini API或DeepSeek API）进行通信。这些密钥不会被发送到本应用开发者或任何第三方服务器。所有AI交互均直接在用户浏览器和相应的AI服务提供商之间进行。
