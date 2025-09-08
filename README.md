<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./static/browser-use-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="./static/browser-use.png">
  <img alt="Shows a black Browser Use Logo in light color mode and a white one in dark color mode." src="./static/browser-use.png"  width="full">
</picture>

<h1 align="center">让 AI 掌控你的浏览器 🤖</h1>

> [!NOTE]
> 本仓库旨在提供 [docs.browser-use.com](https://docs.browser-use.com/) 的中文版本，由 [zdoc.app](https://zdoc.app/) 提供翻译。

## 如何使用中文文档

```sh
git clone https://github.com/zdocapp/browser-use-zh.git # 克隆本仓库

cd browser-use-zh/docs # 进入 docs 目录

npm i -g mintlify # 全局安装 mintlify (一个文档站工具，类似于 VitePress)

mintlify dev # 启动预览

# 访问：http://localhost:3000 查看中文文档
```

[![GitHub stars](https://img.shields.io/github/stars/gregpr07/browser-use?style=social)](https://github.com/gregpr07/browser-use/stargazers)
[![Discord](https://img.shields.io/discord/1303749220842340412?color=7289DA&label=Discord&logo=discord&logoColor=white)](https://link.browser-use.com/discord)
[![Cloud](https://img.shields.io/badge/Cloud-☁️-blue)](https://cloud.browser-use.com)
[![Documentation](https://img.shields.io/badge/Documentation-📕-blue)](https://docs.browser-use.com)
[![Twitter Follow](https://img.shields.io/twitter/follow/Gregor?style=social)](https://x.com/intent/user?screen_name=gregpr07)
[![Twitter Follow](https://img.shields.io/twitter/follow/Magnus?style=social)](https://x.com/intent/user?screen_name=mamagnus00)
[![Weave Badge](https://img.shields.io/endpoint?url=https%3A%2F%2Fapp.workweave.ai%2Fapi%2Frepository%2Fbadge%2Forg_T5Pvn3UBswTHIsN1dWS3voPg%2F881458615&labelColor=#EC6341)](https://app.workweave.ai/reports/repository/org_T5Pvn3UBswTHIsN1dWS3voPg/881458615)

<!-- Keep these links. Translations will automatically update with the README. -->

[德语](https://www.readme-i18n.com/browser-use/browser-use?lang=de) |
[西班牙语](https://www.readme-i18n.com/browser-use/browser-use?lang=es) |
[法语](https://www.readme-i18n.com/browser-use/browser-use?lang=fr) |
[日语](https://www.readme-i18n.com/browser-use/browser-use?lang=ja) |
[韩语](https://www.readme-i18n.com/browser-use/browser-use?lang=ko) |
[葡萄牙语](https://www.readme-i18n.com/browser-use/browser-use?lang=pt) |
[俄语](https://www.readme-i18n.com/browser-use/browser-use?lang=ru) |
[中文](https://www.readme-i18n.com/browser-use/browser-use?lang=zh)

🌤️ 想要跳过设置？使用我们的<b>[云端服务](https://cloud.browser-use.com)</b>，获得更快、可扩展、支持隐身模式的浏览器自动化！

## 🎉 开源 Twitter 黑客马拉松

我们刚刚获得了 **69,000 个 GitHub ⭐**！
为庆祝这一里程碑，我们推出 **#nicehack69** —— 一场以 Twitter 为主的黑客马拉松，奖金池高达 **6,900 美元**。大胆梦想，向我们展示超越演示的 browser-use 智能体的未来！

**截止日期：2025 年 9 月 10 日**

**[🚀 加入黑客马拉松 →](https://github.com/browser-use/nicehack69)**

<div align="center">
<a href="https://github.com/browser-use/nicehack69">
<img src="./static/NiceHack69.png" alt="NiceHack69 Hackathon" width="600"/>
</a>
</div>

> **🚀 使用最新版本！**
>
> 我们每天都会发布针对**速度**、**准确性**和**用户体验**的改进。
>
> ```bash
> pip install --upgrade browser-use
> ```

# 新用户快速入门

使用 pip (Python>=3.11)：

```bash
pip install browser-use
```

如果您尚未安装 Chrome 或 Chromium，也可以使用 playwright 的安装快捷方式下载最新版 Chromium：

```bash
uvx playwright install chromium --with-deps --no-shell
```

启动您的智能体：

```python
import asyncio
from dotenv import load_dotenv
load_dotenv()
from browser_use import Agent, ChatOpenAI

async def main():
    agent = Agent(
        task="Find the number of stars of the browser-use repo",
        llm=ChatOpenAI(model="gpt-4.1-mini"),
    )
    await agent.run()

asyncio.run(main())
```

将您要使用的服务提供商的 API 密钥添加到 `.env` 文件中。

```bash
OPENAI_API_KEY=
```

如需了解其他设置、模型及更多信息，请查阅[文档 📕](https://docs.browser-use.com)。

# 演示示例

<br/><br/>

[任务](https://github.com/browser-use/browser-use/blob/main/examples/use-cases/shopping.py)：将杂货商品加入购物车并完成结账。

[![AI 帮我采购杂货](https://github.com/user-attachments/assets/a0ffd23d-9a11-4368-8893-b092703abc14)](https://www.youtube.com/watch?v=L2Ya9PYNns8)

<br/><br/>

提示：将我最新的 LinkedIn 关注者添加到 Salesforce 的潜在客户中。

![LinkedIn 到 Salesforce](https://github.com/user-attachments/assets/50d6e691-b66b-4077-a46c-49e9d4707e07)

<br/><br/>

[提示](https://github.com/browser-use/browser-use/blob/main/examples/use-cases/find_and_apply_to_jobs.py)：阅读我的简历并寻找机器学习职位，将其保存至文件，然后在新标签页中开始申请。如需帮助，请向我询问。

https://github.com/user-attachments/assets/171fb4d6-0355-46f2-863e-edb04a828d04

<br/><br/>

[提示](https://github.com/browser-use/browser-use/blob/main/examples/browser/real_browser.py)：在 Google 文档中给我的爸爸写一封感谢信，感谢他的一切，并将文档保存为 PDF 格式。

![给爸爸的信](https://github.com/user-attachments/assets/242ade3e-15bc-41c2-988f-cbc5415a66aa)

<br/><br/>

[Prompt](https://github.com/browser-use/browser-use/blob/main/examples/custom-functions/save_to_file_hugging_face.py): 在 Hugging Face 上查找许可证为 cc-by-sa-4.0 的模型，按点赞数排序，将前 5 名保存到文件。

https://github.com/user-attachments/assets/de73ee39-432c-4b97-b4e8-939fd7f323b3

<br/><br/>

## 更多示例

更多示例请查看 [examples](examples) 文件夹或加入 [Discord](https://link.browser-use.com/discord) 展示您的项目。您还可以查看我们的 [`awesome-prompts`](https://github.com/browser-use/awesome-prompts) 仓库获取提示灵感。

## MCP 集成

Browser-use 支持 [模型上下文协议 (MCP)](https://modelcontextprotocol.io/)，可与 Claude Desktop 及其他 MCP 兼容客户端集成。

### 作为 MCP 服务器与 Claude Desktop 配合使用

将 browser-use 添加到您的 Claude Desktop 配置中：

```json
{
  "mcpServers": {
    "browser-use": {
      "command": "uvx",
      "args": ["browser-use[cli]", "--mcp"],
      "env": {
        "OPENAI_API_KEY": "sk-..."
      }
    }
  }
}
```

这使 Claude Desktop 能够访问浏览器自动化工具，用于网页抓取、表单填写等功能。

### 将外部 MCP 服务器连接到 Browser-Use 代理

Browser-use 代理可以连接多个外部 MCP 服务器以扩展其功能：

```python
import asyncio
from browser_use import Agent, Tools, ChatOpenAI
from browser_use.mcp.client import MCPClient

async def main():
    # Initialize tools
    tools = Tools()

    # Connect to multiple MCP servers
    filesystem_client = MCPClient(
        server_name="filesystem",
        command="npx",
        args=["-y", "@modelcontextprotocol/server-filesystem", "/Users/me/documents"]
    )

    github_client = MCPClient(
        server_name="github",
        command="npx",
        args=["-y", "@modelcontextprotocol/server-github"],
        env={"GITHUB_TOKEN": "your-github-token"}
    )

    # Connect and register tools from both servers
    await filesystem_client.connect()
    await filesystem_client.register_to_tools(tools)

    await github_client.connect()
    await github_client.register_to_tools(tools)

    # Create agent with MCP-enabled tools
    agent = Agent(
        task="Find the latest pdf report in my documents and create a GitHub issue about it",
        llm=ChatOpenAI(model="gpt-4.1-mini"),
        tools=tools  # Tools has tools from both MCP servers
    )

    # Run the agent
    await agent.run()

    # Cleanup
    await filesystem_client.disconnect()
    await github_client.disconnect()

asyncio.run(main())
```

详情请参阅 [MCP 文档](https://docs.browser-use.com/customize/mcp-server)。

# 愿景

告诉您的计算机要做什么，它就会完成。

## 路线图

### 代理

- [ ] 使代理速度提升 3 倍
- [ ] 减少 token 消耗（系统提示、DOM 状态）

### DOM 提取

- [ ] 支持与所有 UI 元素进行交互
- [ ] 改进 UI 元素的状态表示，使任何 LLM 都能理解页面内容

### 工作流程

- [ ] 允许用户记录工作流程 - 可通过 browser-use 作为备选方案重新运行

### 用户体验

- [ ] 为教程执行、求职申请、QA 测试、社交媒体等场景创建多种模板，用户可直接复制粘贴使用

### 并行化

- [ ] 人类工作是顺序进行的。浏览器代理的真正威力在于能够并行处理相似任务。例如，如需查找 100 家公司的联系信息，这些任务可全部并行执行并将结果汇报给主代理，由主代理处理结果并再次启动并行子任务。

## 参与贡献

我们欢迎贡献！欢迎提交错误报告或功能需求的 issue。如需参与文档建设，请查看 `/docs` 文件夹。

## 🧪 如何使您的代理更稳健？

我们提供在 CI 中运行您的任务的服务——每次更新时自动执行！

- **添加任务：** 在 `tests/agent_tasks/` 目录中添加 YAML 文件（详情请参阅[`该处的 README`](tests/agent_tasks/README.md)）。
- **自动验证：** 每次推送更新时，您的任务将由代理运行并根据您的标准进行评估。

## 本地设置

要深入了解该库，请查看[本地设置 📕](https://docs.browser-use.com/development/local-setup)。

`main` 是主要开发分支，会频繁更新。生产环境请安装稳定的[版本化发布](https://github.com/browser-use/browser-use/releases)。

---

## 周边商品

想要展示你的 Browser-use 周边吗？来看看我们的[商品商店](https://browsermerch.com)。优秀贡献者将免费获得周边商品 👀。

## 引用说明

如果在研究或项目中使用 Browser Use，请引用：

```bibtex
@software{browser_use2024,
  author = {Müller, Magnus and Žunič, Gregor},
  title = {Browser Use: Enable AI to control your browser},
  year = {2024},
  publisher = {GitHub},
  url = {https://github.com/browser-use/browser-use}
}
```

<div align="center"> <img src="https://github.com/user-attachments/assets/06fa3078-8461-4560-b434-445510c1766f" width="400"/>

[![Twitter Follow](https://img.shields.io/twitter/follow/Gregor?style=social)](https://x.com/intent/user?screen_name=gregpr07)
[![Twitter Follow](https://img.shields.io/twitter/follow/Magnus?style=social)](https://x.com/intent/user?screen_name=mamagnus00)

</div>

<div align="center">
苏黎世与旧金山 ❤️ 倾情打造
 </div>
