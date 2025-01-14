# 为计算器项目做贡献

[english](CONTRIBUTING.md)

计算器团队鼓励社区反馈和贡献。感谢您对改进计算器的兴趣！您可以通过多种方式参与进来。

## 报告问题和建议新功能

如果计算器无法正常工作，请在 [反馈中心](https://insider.windows.com/en-us/fb/?contextid=130&newFeedback=True) 提交报告。反馈中心报告会自动包含诊断数据，例如您使用的计算器版本。

我们很高兴听到您对计算器未来的想法。请查看 [反馈中心](https://insider.windows.com/en-us/fb/?contextid=130)，看看是否有其他人提交了类似的反馈。您可以为现有反馈投票或提交新的建议。

我们在决定下一步工作时总是会查看反馈中心中投票较高的项目。我们会阅读反馈中心和 GitHub 中的评论，并期待听到您的意见。请记住，所有社区互动都必须遵守 [行为准则](CODE_OF_CONDUCT.md)。

## 寻找您可以帮助解决的问题

想找点事情做吗？标记为 [``good first issue``](https://github.com/Microsoft/calculator/labels/good%20first%20issue) 的问题是一个好的起点。

您还可以查看 [``help wanted``](https://github.com/Microsoft/calculator/labels/help%20wanted) 标签，找到其他需要帮助的问题。如果您有兴趣解决某个问题，请留言让大家知道，以避免重复劳动。

## 我们接受的贡献

我们欢迎您对计算器项目的贡献，特别是修复错误和解决用户报告的主要问题的一些改进。以下是一些一般指南：

* **请** 每个 Issue 创建一个拉取请求，并确保在拉取请求中链接该 Issue。
* **请** 遵循我们的 [编码和样式](#style-guidelines) 指南，并尽量保持代码更改尽可能小。
* **请** 尽可能包含相应的测试。
* **请** 在提交 PR 之前检查代码库的其他部分是否存在相同问题。
* **请** 在拉取请求中 [链接您正在解决的问题](https://github.com/blog/957-introducing-issue-mentions)。
* **请** 为您的拉取请求写一个好的描述。描述越详细越好。描述 *为什么* 进行更改以及 *为什么* 选择特定的解决方案。描述您为验证更改而进行的任何手动测试。
* **请勿** 提交未链接到标记为 [`triage approved`](https://github.com/Microsoft/calculator/issues?q=is%3Aissue+is%3Aopen+label%3A%22Triage%3A+Approved%22) 的 Issue 的 PR。这使我们能够在任何人投入时间进行实现之前对想法进行讨论。
* **请勿** 将多个更改合并到一个 PR 中，除非它们具有相同的根本原因。
* **请勿** 提交纯格式/拼写错误更改，除非它们是对已修改代码的其他更改。

我们遵循 [以用户为中心的开发流程](docs/NewFeatureProcess.md)。新功能需要计算器团队的支持，但我们欢迎社区在流程的许多阶段进行贡献。

> 提交针对已批准 Issue 的拉取请求并不保证它会被批准。
> 更改必须符合我们的高标准，包括代码质量、架构和性能，以及 [其他要求](#docs/NewFeatureProcess.md#technical-review)。

## 修改代码

### 准备您的开发环境

要了解如何构建代码和运行测试，请按照 [README](README.md) 中的说明进行操作。

### 样式指南

本项目中的代码使用了几种不同的编码风格，具体取决于代码的年龄和历史。请尽量匹配周围代码的风格。在新组件中，优先使用 [C++ 核心指南](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines) 和 [现代 C++/WinRT 语言投影](https://docs.microsoft.com/en-us/windows/uwp/cpp-and-winrt-apis/) 中描述的模式。

### 测试

您的更改应尽可能包含验证新功能的测试。代码应结构化，以便可以独立于 UI 进行单元测试。[手动测试用例](docs/ManualTests.md) 应在自动化测试不可行的情况下使用。

### Git 工作流程

计算器使用 [GitHub flow](https://guides.github.com/introduction/flow/)，大多数开发直接在 `main` 分支上进行。`main` 分支应始终处于健康状态，随时可以发布。

如果您的更改很复杂，请在提交拉取请求之前清理分支历史。您可以使用 [git rebase](https://docs.microsoft.com/en-us/azure/devops/repos/git/rebase#squash-local-commits) 将更改分组为少量提交，以便我们逐一审查。

在完成拉取请求时，我们通常会将您的更改压缩为一个提交。如果您的拉取请求需要作为单独的提交合并，请告知我们。

## 审查流程

提交拉取请求后，计算器团队的成员将审查您的代码。我们会将请求分配给适当的审查员。任何社区成员都可以参与审查，但最终至少有一名计算器团队成员会批准请求。

通常，需要多次迭代来响应审查员的反馈。尝试查看 [过去的拉取请求](https://github.com/Microsoft/calculator/pulls?q=is%3Apr+is%3Aclosed)，了解可能的体验。

## 贡献者许可协议

在我们审查和接受您的拉取请求之前，您需要签署贡献者许可协议 (CLA)。CLA 确保社区可以自由使用您的贡献。有关协议的更多信息，请访问 [Microsoft 网站](https://cla.opensource.microsoft.com/)。签署 CLA 是一个自动化过程，您只需为 GitHub 上的 Microsoft 项目签署一次。

在您准备创建拉取请求之前，您不需要签署 CLA。当您的拉取请求创建时，它会被一个机器人分类。如果更改是微不足道的（例如，您只是修正了一个拼写错误），那么机器人会将 PR 标记为 `cla-not-required`。否则，它会被分类为 `cla-required`。在这种情况下，系统还会告诉您如何签署 CLA。一旦您签署了 CLA，当前和所有未来的拉取请求将被标记为 `cla-signed`。