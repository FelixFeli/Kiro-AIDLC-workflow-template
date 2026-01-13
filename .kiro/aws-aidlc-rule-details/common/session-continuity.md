# 会话连续性模板

## 欢迎回来提示模板
当用户返回继续现有 AI-DLC 项目的工作时，呈现此提示：

```markdown
**欢迎回来！我可以看到您有一个正在进行的 AI-DLC 项目。**

基于您的 aidlc-state.md，这是您的当前状态：
- **项目**：[项目名称]
- **当前阶段**：[启动/构建/运营]
- **当前阶段**：[阶段名称]
- **最后完成**：[最后完成的步骤]
- **下一步**：[要处理的下一步]

**您今天想要处理什么？**

A) 从中断处继续（[下一步描述]）
B) 回顾先前的阶段（[显示可用阶段]）

[Answer]: 
```

## 必须：会话连续性说明
1. **检测到现有项目时始终首先读取 aidlc-state.md**
2. **从工作流文件解析当前状态**以填充提示
3. **必须：加载先前阶段工件** - 在恢复任何阶段之前，自动读取先前阶段的所有相关工件：
   - **逆向工程**：读取 architecture.md、code-structure.md、api-documentation.md
   - **需求分析**：读取 requirements.md、requirement-verification-questions.md
   - **用户故事**：读取 stories.md、personas.md、story-generation-plan.md
   - **应用程序设计**：读取应用程序设计工件（components.md、component-methods.md、services.md）
   - **设计（单元）**：读取 unit-of-work.md、unit-of-work-dependency.md、unit-of-work-story-map.md
   - **每单元设计**：读取 functional-design.md、nfr-requirements.md、nfr-design.md、infrastructure-design.md
   - **代码阶段**：读取所有代码文件、计划和所有先前工件
4. **按阶段智能上下文加载**：
   - **早期阶段（工作区检测、逆向工程）**：加载工作区分析
   - **需求/故事**：加载逆向工程 + 需求工件
   - **设计阶段**：加载需求 + 故事 + 架构 + 设计工件
   - **代码阶段**：加载所有工件 + 现有代码文件
5. **基于架构选择和当前阶段调整选项**
6. **显示具体的下一步**而不是通用描述
7. **在 audit.md 中记录连续性提示**并包含时间戳
8. **上下文摘要**：加载工件后，为用户提供已加载内容的简要摘要
9. **提问**：始终通过将问题放在 .md 文件中来提出澄清或用户反馈问题。不要在聊天会话中内联放置多选问题。

## 错误处理
如果在会话恢复期间工件丢失或损坏，请参见 [error-handling.md](error-handling.md) 获取恢复程序指导。 