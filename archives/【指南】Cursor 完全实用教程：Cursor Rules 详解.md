# 【指南】Cursor 完全实用教程：Cursor Rules 详解

大家好，我是章北海。

之前在文章中多次提及 **Cursor** 这款神级代码编辑器，它凭借强大的 AI 辅助功能，已经成为许多开发者的首选工具。今天，我们将深入探讨 Cursor 中的 **Rules for AI** 和 **.cursorrules** 文件，以及它们的关系、优先顺序和具体用法。

## 什么是 Rules for AI？

**Rules for AI** 是一种类似于系统提示（system prompt）的功能。通过在设置中填写规则，这些规则会在 **Cursor Chat** 和 **Ctrl/⌘ K** 操作时生效。简单来说，它可以帮助你定制 AI 的行为，使其生成更符合你需求的代码。



## .cursorrules 文件的作用

**.cursorrules** 文件则进一步细化了 AI 的行为定制。它在项目根目录中创建，用于根据项目的特定需求调整 AI 的响应。

主要有以下几点作用：

- **定制 AI 行为**：根据项目需求调整 AI 的响应，确保生成更相关和准确的代码建议。
- **一致性**：通过定义编码标准和最佳实践，确保 AI 生成的代码与项目样式保持一致。
- **上下文意识**：提供项目的重要上下文信息，如常用方法、架构决策或特定库，使 AI 生成的代码更具洞察力。
- **提高生产力**：通过明确的规则，减少手动编辑的需要，加速开发过程。
- **团队对齐**：在团队项目中，共享 .cursorrules 文件可以确保所有成员获得一致的 AI 辅助，促进编码实践的一致性。
- **项目特定知识**：包含有关项目结构、依赖关系或独特需求的信息，帮助 AI 提供更准确和相关建议。

## .cursorrules 文件的使用方法

**.cursorrules** 文件的使用非常简单。你可以在项目根目录中创建一个 `.cursorrules` 文件，并根据需要填写规则。例如：

plaintext
# .cursorrules 文件示例
coding_standard: PEP8
preferred_libraries: pandas, numpy
architecture: microservices


如果你不想手动编写，也可以通过以下方式获取：

1. 访问 [cursor.directory](https://cursor.directory)，从网站中复制对应项目的 **prompt** 并粘贴到 `.cursorrules` 文件中。
   
2. 从 [GitHub](https://github.com/PatrickJS/awesome-cursorrules/tree/main/rules) 直接下载 `.cursorrules` 文件到项目根目录。

## Rules for AI 与 .cursorrules 的优先级

根据测试，**Rules for AI** 和 **.cursorrules** 的优先级如下：

1. **Rules for AI** 优先于 `.cursorrules` 文件。
2. 在工作空间中，第一个文件夹下的 `.cursorrules` 文件会生效。

需要注意的是，如果你的工作空间中有多个仓库（例如后端和前端），每个仓库可能都有自己的 `.cursorrules` 文件。然而，目前无法同时让多个 `.cursorrules` 文件生效。

## 高效开发的小技巧

为了更好地利用 **Cursor** 的 AI 功能，建议结合 **Rules for AI** 和 `.cursorrules` 文件，针对不同项目定制 AI 的行为。这将极大提高开发效率，减少重复劳动。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)

希望这篇教程能帮助你更好地理解和使用 Cursor 的 AI 功能，提升你的开发效率！