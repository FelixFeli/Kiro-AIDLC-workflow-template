# Kiro IDE 的 AI-DLC 工作流模板

为 Kiro IDE 预配置的 AI-DLC（AI驱动的开发生命周期）工作流模板。此模板提供了一个智能的软件开发工作流，能够适应您的需求，保持质量标准，并让您始终掌控开发过程。

## 关于 AI-DLC

AI-DLC 是一种智能软件开发方法论，从概念到部署全程指导您完成结构化的开发阶段。有关该方法论的更多详细信息，请阅读 [AI-DLC 博客](https://aws.amazon.com/blogs/devops/ai-driven-development-life-cycle/) 和 [方法定义论文](https://prod.d13rzhkk8cj2z0.amplifyapp.com/)。

## 快速开始

### 在 Kiro IDE 中使用此模板

1. **克隆此仓库** 获取预配置的 AI-DLC 工作流：
   ```bash
   git clone https://github.com/FelixFeli/Kiro-AIDLC-workflow-template.git
   cd Kiro-AIDLC-workflow-template
   ```

2. **在 Kiro IDE 中打开** - AI-DLC 引导文件已在 `.kiro/steering/` 中配置完成

3. **开始您的项目** 在 Kiro 聊天中输入：
   ```
   Using AI-DLC, [描述您的项目需求]
   ```

4. **遵循引导工作流** - AI-DLC 将自动激活并引导您完成结构化阶段

### 预配置内容

此模板包含：
- ✅ `.kiro/steering/aws-aidlc-rules/` 中的 AI-DLC 引导文件
- ✅ `.kiro/aws-aidlc-rule-details/` 中的规则详情
- ✅ 适用于 Kiro IDE 的正确目录结构
- ✅ 即用型工作流激活配置

## 三阶段自适应工作流

AI-DLC 遵循适应项目复杂性的结构化方法：

### 🔵 启动阶段
**确定构建什么以及为什么**
- 工作区检测（绿地项目 vs 棕地项目）
- 逆向工程（针对现有代码库）
- 需求分析和验证
- 用户故事创建（适用时）
- 应用程序设计和工作单元规划
- 带有可视化路线图的工作流规划

### 🟢 构建阶段
**确定如何构建**
- 每个单元的功能设计
- 非功能性需求（NFR）分析
- 基础设施设计
- 带有全面规划的代码生成
- 构建和测试指令生成

### 🟡 运营阶段
**部署和监控（未来扩展）**
- 部署自动化规划
- 监控和可观察性设置
- 生产就绪验证

## 核心特性

- **🎯 自适应智能**：仅执行对您的特定请求有价值的阶段
- **🧠 上下文感知**：分析现有代码库和复杂性要求
- **⚖️ 基于风险**：复杂变更获得全面处理，简单变更保持高效
- **❓ 问题驱动**：结构化多选题确保清晰度
- **🎮 始终掌控**：审查执行计划并批准每个阶段
- **📋 完整审计跟踪**：在 `aidlc-docs/audit.md` 中完整跟踪决策和进度

## 使用示例

### 启动新项目
```
Using AI-DLC, 创建一个带有用户认证的任务管理系统 REST API
```

### 增强现有代码
```
Using AI-DLC, 为我现有的聊天应用添加实时通知功能
```

### 错误调查
```
Using AI-DLC, 调查并修复用户仪表板中的性能问题
```

## 生成的工件

所有 AI-DLC 工件都组织在 `aidlc-docs/` 目录中：

```
aidlc-docs/
├── inception/           # 🔵 规划阶段工件
│   ├── plans/
│   ├── reverse-engineering/  # 针对现有代码库
│   ├── requirements/
│   ├── user-stories/
│   └── application-design/
├── construction/        # 🟢 构建阶段工件
│   ├── plans/
│   ├── {单元名称}/
│   │   ├── functional-design/
│   │   ├── nfr-requirements/
│   │   ├── nfr-design/
│   │   ├── infrastructure-design/
│   │   └── code/
│   └── build-and-test/
├── operations/          # 🟡 未来部署工件
├── aidlc-state.md      # 工作流进度跟踪
└── audit.md            # 完整决策审计跟踪
```

## 最佳实践

1. **具体明确**：在初始请求中提供清晰、详细的需求
2. **仔细审查**：在继续之前始终审查并批准每个阶段
3. **积极提问**：使用结构化问答格式进行澄清
4. **跟踪进度**：在 `aidlc-state.md` 中监控工作流状态
5. **保持控制**：您可以根据需要请求更改或跳过阶段

## 前提条件

- 已安装并配置 [Kiro IDE](https://kiro.dev/)
- 对项目需求有基本了解
- 愿意参与结构化问答以获得最佳结果

## 故障排除

### AI-DLC 未激活？
- 确保您的消息以 "Using AI-DLC, ..." 开头
- 检查 `.kiro/steering/` 中是否存在引导文件
- 验证 Kiro IDE 是否正确配置

### 缺少工件？
- 检查 `aidlc-docs/` 目录结构
- 查看 `audit.md` 了解执行历史
- 确保每个阶段都已正确批准

## 贡献

此模板专为 Kiro IDE 用户设计。如需改进或报告问题：
1. Fork 此仓库
2. 进行您的更改
3. 提交带有详细描述的 pull request

## 许可证

此模板采用 MIT-0 许可证。详情请参阅 LICENSE 文件。

---

**准备开始了吗？** 在 Kiro IDE 中打开此项目并输入：`Using AI-DLC, [您的项目描述]`
