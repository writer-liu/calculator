# 计算器

[**english**](/calculator-main//README.md)

Windows 计算器应用程序是一个用 C++ 和 C# 编写的现代 Windows 应用程序，预装在 Windows 系统中。该应用程序提供标准、科学和程序员计算器功能，以及各种单位和货币之间的转换功能。

计算器定期发布新功能和错误修复。您可以在 [Microsoft Store](https://www.microsoft.com/store/apps/9WZDNCRFHVN5) 获取最新版本的计算器。

[![持续集成](https://github.com/microsoft/calculator/actions/workflows/action-ci.yml/badge.svg)](https://github.com/microsoft/calculator/actions/workflows/action-ci.yml)

<img src="docs/Images/CalculatorScreenshot.png" alt="计算器截图" width="450px" />

## 功能
- 标准计算器功能，提供基本操作并在输入时立即评估命令。
- 科学计算器功能，提供扩展操作并使用运算顺序评估命令。
- 程序员计算器功能，提供开发人员常用的数学操作，包括常见进制之间的转换。
- 日期计算功能，提供两个日期之间的差异，以及在给定输入日期上加减年、月和/或天的能力。
- 计算历史和内存功能。
- 各种单位之间的转换。
- 基于 [Bing](https://www.bing.com) 数据的货币转换。
- 基本算术操作（加法、减法、乘法、除法）的[无限精度](https://en.wikipedia.org/wiki/Arbitrary-precision_arithmetic)，确保计算永不失去精度。

## 入门
先决条件：
- 您的计算机必须运行 Windows 11，版本 22000 或更新版本。
- 安装最新版本的 [Visual Studio](https://developer.microsoft.com/en-us/windows/downloads)（免费的社区版即可）。
  - 安装“通用 Windows 平台开发”工作负载。
  - 安装可选的“C++ 通用 Windows 平台工具”组件。
  - 安装最新的 Windows 11 SDK。

  ![Visual Studio 安装截图](docs/Images/VSInstallationScreenshot.png)
- 安装 [XAML Styler](https://marketplace.visualstudio.com/items?itemName=TeamXavalon.XAMLStyler) Visual Studio 扩展。

- 获取代码：
    ```
    git clone https://github.com/Microsoft/calculator.git
    ```

- 在 Visual Studio 中打开 [src\Calculator.sln](/src/Calculator.sln) 以构建和运行计算器应用程序。
- 有关计算器项目架构的一般描述，请参阅 [ApplicationArchitecture.md](docs/ApplicationArchitecture.md)。
- 要运行 UI 测试，您需要确保安装了 [Windows Application Driver (WinAppDriver)](https://github.com/microsoft/WinAppDriver/releases/latest)。

## 贡献
想要贡献？团队鼓励社区反馈和贡献。请遵循我们的[贡献指南](CONTRIBUTING.md)。

如果计算器无法正常工作，请在 [反馈中心](https://insider.windows.com/en-us/fb/?contextid=130) 提交报告。我们也欢迎在 [GitHub 提交问题](https://github.com/Microsoft/calculator/issues)。

## 路线图
有关 Windows 计算器计划和发布时间表的信息，请参阅 [Windows 计算器路线图](docs/Roadmap.md)。

### 图形模式
添加图形计算器功能[在项目路线图上](https://github.com/Microsoft/calculator/issues/338)，我们希望该项目能够围绕图形创建一个出色的最终用户体验。为此，官方内置 Windows 计算器的 UI 目前是该存储库的一部分，尽管驱动 Microsoft Mathematics 和 OneNote 中图形的专有 Microsoft 构建的图形引擎不是。社区成员仍然可以参与 UI 的创建，但由于使用了[引擎的模拟实现](/src/GraphingImpl/Mocks)构建在[通用图形 API](/src/GraphingInterfaces)之上，开发者构建将不具有图形功能。

## 诊断数据
该项目收集使用数据并将其发送给 Microsoft 以帮助改进我们的产品和服务。阅读我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=521839)了解更多信息。诊断数据在开发构建中默认禁用，可以通过 `SEND_DIAGNOSTICS` 构建标志启用。

## 货币转换器
Windows 计算器包括一个货币转换器功能，在开发者构建中使用模拟数据。Microsoft 用于货币转换器功能的数据（例如，在应用程序的零售版本中）未授权您使用。模拟数据将清楚地标识出来，因为它引用的是行星而不是国家，并且无论选择的输入如何都保持静态。

## 报告安全问题
请参阅 [SECURITY.md](./SECURITY.md)。

## 许可证
版权所有 (c) Microsoft Corporation。保留所有权利。

根据 [MIT 许可证](./LICENSE) 许可。