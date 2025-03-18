# LLM-Navigation
## 0. 写在前面

最近学了不少关于大模型的东西，但是随着学得越来越多也越来越杂，有时候想用到之前的一些东西的时候又忘了在哪里，意识到还是需要系统整理与收集一些资料，因此本仓库主要是记录平时的一些学习记录，同时也想通过AI找到另一个自我。



碎碎念：框架也是慢慢搭建

## 1. 基础篇

先补近期学的东西过于基础的后面慢慢补上

- 大模型基础知识
  - Prompt
    - [Prompt Engineering Guide](https://www.promptingguide.ai/)
      - 通过设计和优化提示词来高效利用大语言模型，可以提升其在问答、数学推理、代码生成等复杂任务中的表现。这个项目中有关于大模型的各类基础概念，新手看可能比较坐牢，可以当作后期的字典查询。
    - [System Prompt与User Prompt的使用场景区别](https://github.com/Y4tacker/LLM-Navigation/blob/main/1.%E5%9F%BA%E7%A1%80%E7%AF%87/Prompt/System-Prompt%E4%B8%8EUser-Prompt%E7%9A%84%E4%BD%BF%E7%94%A8%E5%9C%BA%E6%99%AF%E5%8C%BA%E5%88%AB.md)
- RAG
  - [为什么RAG系统"一看就会，一做就废"？](https://mp.weixin.qq.com/s/OEAAzbuCvG3gf_mq_mrlfg)
    - 探讨了检索增强生成（RAG）系统在工程实践中的12个常见问题及其优化策略，涵盖数据清洗、分块处理、嵌入模型选择、元数据使用、多级索引、查询转换、检索参数设置、高级检索策略、重排模型、提示词设计和大语言模型选择等环节。
- Agent
  - [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)
    - 个人看过的关于Agent最好的讲解文章(虽然不是手把手教你如何实现agent，自行百度操作)，本篇中分别介绍了传统工作流式的Agent原理并引入了端到端的Agent理念，深度好文.

- 大模型拓展能力
  - MCP
    - [MCP官方文档](https://modelcontextprotocol.io/introduction)
      - MCP是一个让不同的应用程序和AI模型可以更容易完成行为交互的标准，支持多种传输模式STDIO(本地)和SSE(远程)。(MCP的官方介绍SDK文档，先用起来再具体深入了解他)
    - [MCP：昙花一现还是未来标准？](https://blog.langchain.dev/mcp-fad-or-fixture/)
      - 备注：目前来看MCP的核心价值在于允许用户为不可控的AI代理添加自定义工具，无需修改底层代理逻辑，未来期待能成为和Zapier一样实现真正的低代码。在实际生产中，工具需与系统提示词(未来模型能力提升能弥补)、架构高度定制化，MCP的“即插即用”难以实现。
     
- 其他
  - [wx-bot大模型相关每日资料收集](https://github.com/Y4tacker/LLM-Navigation/blob/main/other/wxbot)
    - 自动爬取的大模型群聊热点讨论内容及链接(非程序文件、仅含分享内容) 

## x. 安全篇

- Prompt注入对抗与防护
  - 攻击篇
    - Prompt注入
      - [Prompt越狱手册](https://acmesec.github.io/AI/PromptJailbreakManual.html#jailbreak)
        - 关于一些常见的提示词越狱攻击手法介绍(只需要从锚点定位处开始阅读即可)
      - [Making Them Ask and Answer: Jailbreaking Large Language Models in Few Queries via Disguise and Reconstruction](https://arxiv.org/abs/2402.18104)
        - 一篇关于提示词注入的顶会文章，简单来说就是利用了LLM的建模中，对查询和补全两部分注意力的分配不同，使得当恶意指令出现在模型补全部分时会产生越狱。(好用！！)
    
  - 防护篇
    - [通过签名解决Prompt注入](https://github.com/Y4tacker/LLM-Navigation/blob/main/resources/pdf/PromptInjection/Signed-Prompt-A-New-Approach-to-Prevent-Prompt-Injection-Attacks-Against%20LLM-Integrated-Applications.pdf)
      - 评价是简单粗暴高成本
  
- 攻防赋能
  - OWASP
    - [GenAI Red Teaming Guide](https://genai.owasp.org/resource/genai-red-teaming-guide/)
      - OWASP出品，概述了GenAI红队的关键组成部分，为网络安全专业人员、AI/ML工程师、红队从业者、风险管理人员、对抗性攻击研究人员、首席信息安全官、架构团队和业务领导者提供了可操作的见解。该指南强调了红队在四个方面的整体方法：模型评估、实施测试、基础设施评估和运行时行为分析。 
  - 先知安全
    - 2025
      - [Ai红队攻防实践](https://github.com/Y4tacker/LLM-Navigation/blob/main/resources/ppt/aisec/2025%E5%B9%B4%E5%85%88%E7%9F%A5%E5%AE%89%E5%85%A8%E6%B2%99%E9%BE%99-Ai%E7%BA%A2%E9%98%9F%E6%94%BB%E9%98%B2%E5%AE%9E%E8%B7%B5.pptx)
      - [AI赋能红队的新优势](https://github.com/Y4tacker/LLM-Navigation/blob/main/resources/ppt/aisec/2025%E5%B9%B4%E5%85%88%E7%9F%A5%E5%AE%89%E5%85%A8%E6%B2%99%E9%BE%99-AI%E8%B5%8B%E8%83%BD%E7%BA%A2%E9%98%9F%E7%9A%84%E6%96%B0%E4%BC%98%E5%8A%BF.pptx)
      - [机遇和挑战：大模型及其生态的安全性和脆弱性](https://github.com/Y4tacker/LLM-Navigation/blob/main/resources/ppt/aisec/2025%E4%BA%91%E5%AE%89%E5%85%A8%E5%A4%A7%E4%BC%9A-%E6%9C%BA%E9%81%87%E5%92%8C%E6%8C%91%E6%88%98-%E5%A4%A7%E6%A8%A1%E5%9E%8B%E5%8F%8A%E5%85%B6%E7%94%9F%E6%80%81%E7%9A%84%E5%AE%89%E5%85%A8%E6%80%A7%E5%92%8C%E8%84%86%E5%BC%B1%E6%80%A7.pptx)


## X.应用篇

Ps: 无意间看到过的比较有趣的项目都会放进来

- Agent
  - [MobileAgent](https://github.com/X-PLUG/MobileAgent)
    - 阿里巴巴通义实验室出品，简单来讲就是通过指令控制手机完成操作，目前最新版也支持了电脑端操作
  - [browser-use](https://github.com/browser-use/browser-use)
    - 让AI控制浏览器，没记错之前manus也是用的这款.同时提供了[webui](https://github.com/browser-use/web-ui)版

- 金融
  - [stocks-insights-ai-agent](https://github.com/vinay-gatech/stocks-insights-ai-agent)
    - 基于LangChain、LangChain实现的股票表现可视化AI大模型股票分析
- 建模
  - [blender-mcp](https://github.com/ahujasid/blender-mcp)
    - 基于MCP实现的通过大模型3D建模 ，炫酷！

## x. 工具/资源篇

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
- Prompt
  - [PromptUP](https://promptup.net/)
    - 一个可以存储并分享Prompt的简单应用.
  
  - [prompt-optimizer](https://github.com/linshenkx/prompt-optimizer)
    - AI应用能力的关键就是能否写出优秀的提示词，我们应该学习一个优秀合格的提示词应该是什么样的，在这个项目我们重点关注源码中提示词优化的Prompt部分即可([点我直达](https://github.com/linshenkx/prompt-optimizer/blob/master/packages/core/src/services/template/defaults.ts))
  
- Model
  - [Awesome-Chinese-LLM](https://github.com/HqWu-HITCS/Awesome-Chinese-LLM)
    - 整理开源的中文大语言模型，以规模较小、可私有化部署、训练成本较低的模型为主，包括底座模型，垂直领域微调及应用，数据集与教程等。
  


## NAN
- [AI防洗稿思路(简单粗暴)](https://mp.weixin.qq.com/s/xO8Zuq26_EYdbv4TWF-YZQ)
