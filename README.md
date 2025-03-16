# LLM-Navigation
## 0. 写在前面

最近学了不少关于大模型的东西，但是随着学得越来越多也越来越杂，有时候想用到之前的一些东西的时候又忘了在哪里，意识到还是需要系统整理与收集一些资料，因此本仓库主要是记录平时的一些学习记录，同时也想通过AI找到另一个自我。



碎碎念：框架也是慢慢搭建

## 1. 基础篇

先补近期学的东西过于基础的后面慢慢补上

- 大模型拓展能力
  - MCP
    - [MCP官方文档](https://modelcontextprotocol.io/introduction)
      - MCP是一个让不同的应用程序和AI模型可以更容易完成行为交互的标准，支持多种传输模式STDIO(本地)和SSE(远程)。(MCP的官方介绍SDK文档，先用起来再具体深入了解他)
    - [MCP：昙花一现还是未来标准？](https://blog.langchain.dev/mcp-fad-or-fixture/)
      - 备注：目前来看MCP的核心价值在于允许用户为不可控的AI代理添加自定义工具，无需修改底层代理逻辑，未来期待能成为和Zapier一样实现真正的低代码。在实际生产中，工具需与系统提示词(未来模型能力提升能弥补)、架构高度定制化，MCP的“即插即用”难以实现。

## x. 安全篇

- Prompt注入对抗与防护
  - 防护篇
    - [通过签名解决Prompt注入，评价是简单粗暴高成本](https://github.com/Y4tacker/LLM-Navigation/blob/main/resources/pdf/PromptInjection/Signed-Prompt-A-New-Approach-to-Prevent-Prompt-Injection-Attacks-Against%20LLM-Integrated-Applications.pdf)

## X.应用篇

Ps: 无意间看到过的比较有趣的项目都会放进来

- 提示词
  - [prompt-optimizer](https://github.com/linshenkx/prompt-optimizer)
    - AI应用能力的关键就是能否写出优秀的提示词，列出此项目是为了让大家知道一个优秀合格的提示词应该是什么样的，所以这个项目我们重点关注源码中提示词优化的Prompt即可([点我直达](https://github.com/linshenkx/prompt-optimizer/blob/master/packages/core/src/services/template/defaults.ts))

- 金融
  - [stocks-insights-ai-agent](https://github.com/vinay-gatech/stocks-insights-ai-agent)
    - 基于LangChain、LangChain实现的股票表现可视化AI大模型股票分析
- 建模
  - [blender-mcp](https://github.com/ahujasid/blender-mcp)
    - 基于MCP实现的通过大模型3D建模 ，炫酷！

## x. 工具篇

- Function Calling与MCP
  - MCP
    - MCP Server导航站-懒狗必备不想要自己手搓服务可以直接用现成的，但也需要注意安全问题
      - [Smithery.ai](https://smithery.ai)
        - 华裔青年Henry Mao打造的产品,目前发现交互体验最好的MCP导航网站，每个MCP Server都搭配或生成使用代码.
      - [MCP.so](https://mcp.so/)
        - 独立开发者idoubi开发的 MCP.so 导航，收录了2k多个Server，数量庞大
      - [MCPs.live](http://mcps.live/)
        - 没啥好说的，mcp搜索站
      - [Composio MCP](https://mcp.composio.dev/)
        - 每个MCP都可以生成一个SSE URL，开发者技能在自己应用中集成这个MCP的能力，无需从0开发，但可能需要🪜
      - [Pulse MCP](https://www.pulsemcp.com/)
        - 已收录了1500+个Server，比较特别的是，网站提供了很多Use Case，让人更直观了解怎么用


## NAN

- [AI防洗稿思路(简单粗暴)](https://mp.weixin.qq.com/s/xO8Zuq26_EYdbv4TWF-YZQ)
