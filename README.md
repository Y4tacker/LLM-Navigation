# LLM-Navigation
## 0. 写在前面

最近学了不少关于大模型的东西，但是随着学得越来越多也越来越杂，有时候想用到之前的一些东西的时候又忘了在哪里，意识到还是需要系统整理与收集一些资料，因此本仓库主要是记录平时的一些学习记录，同时也想通过AI找到另一个自我。

<p align="right">2025年3月16日</p>


碎碎念：框架也是慢慢搭建

## 1. 基础篇

先补近期学的东西过于基础的后面慢慢补上

- 大模型基础知识
  - 通用类
    - [【2万字】一文搞懂：大模型是怎么被训练出来的？AI大模型落地必读](https://mp.weixin.qq.com/s/o7QqcohmVJ-0ml4V-BM7Sg)
      - 详细介绍了大语言模型（LLM）的基本原理、训练步骤及关键技术，包括预训练、微调、强化学习（RL）和基于人类反馈的强化学习（RLHF），并探讨了如何通过这些方法提升模型性能和减少幻觉问题。同时也介绍了Deepseek的GRPO算法对RL的优化.
  - Prompt
    - [Prompt Engineering Guide](https://www.promptingguide.ai/)
      - 通过设计和优化提示词来高效利用大语言模型，可以提升其在问答、数学推理、代码生成等复杂任务中的表现。这个项目中有关于大模型的各类基础概念，新手看可能比较坐牢，可以当作后期的字典查询。
    - [System Prompt与User Prompt的使用场景区别](https://github.com/Y4tacker/LLM-Navigation/blob/main/1.%E5%9F%BA%E7%A1%80%E7%AF%87/Prompt/knowledge/System-Prompt%E4%B8%8EUser-Prompt%E7%9A%84%E4%BD%BF%E7%94%A8%E5%9C%BA%E6%99%AF%E5%8C%BA%E5%88%AB.md)
    
    - [提示词优秀模板](https://github.com/Y4tacker/LLM-Navigation/tree/main/1.%E5%9F%BA%E7%A1%80%E7%AF%87/Prompt/prompt-examples)
      - 平时看到的各个地方的写的不错的提示词，统一整理到此目录下(佛系更新).
- RAG(选看)
  - [为什么RAG系统"一看就会，一做就废"？](https://mp.weixin.qq.com/s/OEAAzbuCvG3gf_mq_mrlfg)
    - 探讨了检索增强生成（RAG）系统在工程实践中的12个常见问题及其优化策略，涵盖数据清洗、分块处理、嵌入模型选择、元数据使用、多级索引、查询转换、检索参数设置、高级检索策略、重排模型、提示词设计和大语言模型选择等环节。
  - [高阶RAG技巧：探索提升RAG系统性能的不同技巧](https://mp.weixin.qq.com/s/VZq2zsuJGsGaYTx6POqUzg)
    - 和上一篇类似，详细介绍了通过索引优化、预检索优化、检索优化和后检索优化等高级技术来提升RAG系统性能的方法，从而提高检索准确性和生成响应的质量。
  - [为什么RAG一定需要Rerank？](https://mp.weixin.qq.com/s/qUBVRIt-QNgxLW8HHqybMw)
    - 本文探讨了在检索增强生成（RAG）系统中，当单纯依赖向量搜索和大语言模型（LLM）无法达到理想效果时，如何通过引入重排序（Rerank）技术来提升性能，解决召回率与上下文窗口限制之间的矛盾，并详细解释了Rerank的原理、优势及其在两阶段检索系统中的应用。不过没有实际例子，当科普文学习即可.
  - [大模型 RAG 终极指南：信息检索 + 文本向量化 + BGE-M3 实践全解析！](https://mp.weixin.qq.com/s/0mfzH2NsbwSMEb-ArLt9Jg)
    - 系统梳理了RAG技术中的关键知识点，重点解析了信息检索的三大发展阶段、三种embedding类型的工作原理及对比，以及BGE-M3模型的结构、精调方法和reranker重排序机制，为读者掌握文本向量化和信息检索技术提供了全面的理论与实践指导。
  - 实操系列-[RAG101](https://github.com/realyinchen/RAG/blob/main/RAG101)
    - [RAG101第一课：一个简单的RAG工作流](https://mp.weixin.qq.com/s?__biz=MzI2ODUyMTQyNA==&mid=2247496679&idx=1&sn=d61b86f055641fcb858a895d18d759cc&chksm=eaece958dd9b604e545d8aad12ff847454515af6621b7607ca7f0f111407c17aa0634373707c&cur_album_id=3689450339863740420&scene=189#wechat_redirect)
      - RAG101系列教程的开篇，详细讲解了如何构建一个简单的RAG系统，包括文档加载、文本拆分、嵌入处理、语义检索和检索增强生成等关键步骤，并提供了代码示例和源码链接。
    - [RAG101第二课：一个简单的CSV文件RAG工作流](https://mp.weixin.qq.com/s?__biz=MzI2ODUyMTQyNA==&mid=2247496765&idx=1&sn=afad66a3ce572217c0a4fa134b5ccb51&chksm=eaecee82dd9b6794a905bc0280f54f770051c0fdf8615442f21d99b2fa4e818e4f62472367d7&cur_album_id=3689450339863740420&scene=189#wechat_redirect)
      - 没有基础概念，仅仅是教你如何建立一个针对CSV文件的RAG工作流。
    - [RAG101第三课：通过添加验证和优化构建可靠的RAG](https://mp.weixin.qq.com/s/afffaj0q08rJZN5LAgaz_w)
      - 本文介绍了 Reliable-RAG 方法，通过文档相关性过滤、幻觉检查和片段高亮等步骤改进传统 RAG 系统，提升生成答案的准确性、可靠性和透明度.
- Agent & Agentic & ..
  - Agent
    - [一步步教你如何构建一个通用的大模型智能体（LLM Agent）](https://mp.weixin.qq.com/s/fjVu-sDaOwz3yj3F_YiU9Q)
      - 个人学完感觉非常不错的关于如何设计一个Agent的小白文，文章中详细介绍了构建通用LLM Agent的七个关键步骤：选择合适的LLM、定义控制逻辑与通信结构、制定核心指令、设计并优化工具、制定记忆管理策略、解析Agent输出以及编排下一步操作，同时指出从单Agent原型入手可以为更复杂的多Agent系统奠定基础。
    - [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)
      - 个人看过的关于Agent最好的讲解文章(虽然不是手把手教你如何实现agent，自行百度操作)，本篇中分别介绍了传统工作流式的Agent原理并引入了端到端的Agent理念，深度好文.
    - [面向六个月后的 AI Code，也许影响的不只是前端](https://mp.weixin.qq.com/s/_JQDJxnltsnRvsIcHcRsfw)
      - 这篇文章重点看Agent与Workflow的对比部分，思考很彻底
    - [AI Agent 技术栈全景图](https://mp.weixin.qq.com/s/tcmZcAvQxg16aMtoa8X6zw)
      - 全面解析了AI智能体的技术栈和行业格局，详细阐述了从模型服务、存储、工具调用到框架设计和托管部署的各个环节.
    - [理解这10个核心概念，你就学完了OpenAI最新的开源Agents SDK](https://mp.weixin.qq.com/s/_Rmt2IayeMdWiuzLfKcB3Q)
      - 这篇文章详细解析了OpenAI推出的全新开源Agents SDK的十大关键概念和特性，包括Models、Agents、Runner、Tools、Context、StructuredOutput、Handoffs、Guardrails、Tracing和Orchestrating，并通过一个贯穿始终的案例帮助我们快速掌握这个强大的Agent开发工具。
    - [Why Do Multi-Agent LLM Systems Fail?](https://arxiv.org/html/2503.13657v1)
      - 通过系统分析多智能体大型语言模型系统的执行轨迹，识别出14种失败模式，并将其归类为三大类，提出了第一个结构化的多智能体系统失败分类法（MASFT），并探讨了通过改进规范、角色和对话管理以及验证策略来缓解这些失败模式的可能性和局限性。偷懒的话也可以看这篇[微信公众号总结](https://mp.weixin.qq.com/s/V2kNZxSClDLr8VYRCmwv3g)
  - Agentic
    - TODO
  - MOE
    - [【科普】大模型中常说的 MoE 是指什么？](https://fisherdaddy.com/posts/introduce-moe/)
      - 介绍了混合专家模型（MoE）是什么，同时分析了其工作原理、优劣势及应用领域。
  - 其他
    - [全面对比AI Agent 与 Agentic AI](https://mp.weixin.qq.com/s/1mpAqgtKyhUnkLSc_SiiIQ?token=423077674&lang=zh_CN)
      - 对Agent与Agentic做了概念层的对比：AI Agent是专注于特定任务的智能体，而Agentic AI则是具备高度自主性和适应性的智能系统.
- 大模型拓展能力
  - MCP
    - [MCP官方文档](https://modelcontextprotocol.io/introduction)
      - MCP是一个让不同的应用程序和AI模型可以更容易完成行为交互的标准，支持多种传输模式STDIO(本地)和SSE(远程)。(MCP的官方介绍SDK文档，先用起来再具体深入了解他)
    - [MCP：昙花一现还是未来标准？](https://blog.langchain.dev/mcp-fad-or-fixture/)
      - 备注：目前来看MCP的核心价值在于允许用户为不可控的AI代理添加自定义工具，无需修改底层代理逻辑，未来期待能成为和Zapier一样实现真正的低代码。在实际生产中，工具需与系统提示词(未来模型能力提升能弥补)、架构高度定制化，MCP的“即插即用”难以实现。
  
- 其他
  - [wx-bot大模型相关每日资料收集](https://github.com/Y4tacker/LLM-Navigation/blob/main/other/wxbot)
    - 自动爬取的大模型群聊热点讨论内容及链接(非程序文件、仅含分享内容) 
  - [不再混淆了！一文揭秘MCP Server、Function Call与Agent的核心区别](https://mp.weixin.qq.com/s?__biz=MjM5NTgwODEzMg==&mid=2257484095&idx=1&sn=71284204bf30233d0258f6abb678b390&chksm=a4a5603f364e98ebc5a0e6a337a72513b580c961fe7b88ff3eba431d73d89c750ecb0c8ce666&mpshare=1&scene=1&srcid=0322BijeLC7M69dAiXwYiytL&sharer_shareinfo=63abf444d9577f201e38099732cbe502&sharer_shareinfo_first=63abf444d9577f201e38099732cbe502#rd)
  - [Dify 实现DeepResearch工作流拆解并再看升级版Dify能否搭建出Manus？](https://mp.weixin.qq.com/s/I4HochBCvPf-xUPlSURmlg)
    - 手把手教学关于如何通过一个工作流实现DeepResearch





## x. 安全篇

- Prompt对抗与防护
  - 攻击篇
    - Prompt
      - [Prompt越狱手册](https://acmesec.github.io/AI/PromptJailbreakManual.html#jailbreak)
        - 关于一些常见的提示词越狱攻击手法介绍(只需要从锚点定位处开始阅读即可)
      - [Making Them Ask and Answer: Jailbreaking Large Language Models in Few Queries via Disguise and Reconstruction](https://arxiv.org/abs/2402.18104)
        - 一篇关于提示词注入的顶会文章，简单来说就是利用了LLM的建模中，对查询和补全两部分注意力的分配不同，使得当恶意指令出现在模型补全部分时会产生越狱。(好用！！)
    - 模型安全
      - [模型序列化攻击](https://paper.seebug.org/3298/)
        - 简单探讨了机器学习中多种主流模型序列化攻击的风险和防御措施
    - 应用
      - [Yak支持MCP啦](https://mp.weixin.qq.com/s/FGmpvQKAbKstwkXhOAG4xQ)
        - 指挥yak干活不再是梦.
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
  - [奇御AI安全技术沙龙](https://github.com/Y4tacker/LLM-Navigation/tree/main/resources/pdf/aisec/2025%E5%A5%87%E5%BE%A1AI%E5%AE%89%E5%85%A8%E6%8A%80%E6%9C%AF%E6%B2%99%E9%BE%99)
  - [TVP-AI与安全高峰论坛](https://github.com/Y4tacker/LLM-Navigation/tree/main/resources/pdf/aisec/2025TVP)


## X.应用篇

Ps: 无意间看到过的比较有趣的项目都会放进来

- Agent
  - [MobileAgent](https://github.com/X-PLUG/MobileAgent)
    - 阿里巴巴通义实验室出品，简单来讲就是通过指令控制手机完成操作，目前最新版也支持了电脑端操作
  - [browser-use](https://github.com/browser-use/browser-use)
    - 让AI控制浏览器，没记错之前manus也是用的这款.同时提供了[webui](https://github.com/browser-use/web-ui)版
  - [Browserbase](https://www.browserbase.com/)
    - 一个用于运行无头浏览器的平台,原生兼容Stagehand、Playwright、Puppeteer、Selenium等框架，并有丰富的SDK方便开发.

- 金融
  - [stocks-insights-ai-agent](https://github.com/vinay-gatech/stocks-insights-ai-agent)
    - 基于LangChain、LangChain实现的股票表现可视化AI大模型股票分析
- 建模
  - [blender-mcp](https://github.com/ahujasid/blender-mcp)
    - 基于MCP实现的通过大模型3D建模 ，炫酷！
  
- 生活
  - [浏览器 AI 阅读助手](https://sumbuddy.app/)
    - 一款高度灵活的AI浏览器助手，支持多模型配置、完全自定义提示词、Mermaid图表渲染和对话式总结(因为用户高度自定义，新手还能从中顺手学习提示词的写法)。
  - [AI 9天完成一本书，客单价1万的全流程分享](https://xuqiwei1986.feishu.cn/wiki/JjYHwH29miClbqkDGazc8A8znwf)
    - 这篇文章中我们主要学习的是复杂文本生成任务的AI通用解决思路，可以概括为：**明确目标→任务拆解→指令设计→流程化操作→动态调整→结果验证→服务分级**
- 其他
  - [Jina AI](https://mp.weixin.qq.com/s?__biz=MzkyODIxMjczMA==&mid=2247502419&idx=1&sn=120f53719910bcc2c633b2f831d7a011&chksm=c3f36b9d4e8ad2fec37e6cb12eba991cb578d04aa7acf872de5054510dd7a82b74d8a36e7479&mpshare=1&scene=1&srcid=04020dhXQIX99XWNZX95ZQCv&sharer_shareinfo=f59445cd084556d4135b2607e7b220b0&sharer_shareinfo_first=f59445cd084556d4135b2607e7b220b0#rd)
    - 将 URL 转换为大模型友好输入，这里没有贴官方网站，贴的是官方的公众号的实际应用介绍更深入直观 

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
- [AI工具集](https://ai-bot.cn/)
  - 该收录了数百个国内外不同类型的AI工具，涵盖写作、绘画、图像、视频、办公、对话、编程、设计、音频、搜索、开发平台、法律助手、内容检测、学习网站等多个领域。
