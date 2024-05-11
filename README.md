<div align="center">
<img src="http://k.imiyoo.com/k.png" alt="icon" width="100px"/>
<h1 align="center">KAPI<br>Free-LLM-API</h1>

支持 **OpenAI、智谱AI、月之暗面和零一万物**等大语言模型

[快速开始](#如何使用) / [API文档](https://apifox.com/apidoc/shared-f81e1fd6-279b-4314-9b4d-a5708355fb7e) / [获取免费Key](https://k.imiyoo.com) / [服务可用性](http://43.133.38.250:3001/status/kapi)

</div>

## 数据隐私与安全

KAPI高度重视您的数据隐私保护与安全，对流经网关的数据均进行加密传输和存储，在使用大模型服务过程中，我们并不会要求您提供用户的个人关键隐私信息。在满足当地法律法规前提下，未经您的许可，我们决不会向任何第三方提供有关API调用者的任何关联信息。

但您需要知道，当您在使用第三方大语言模型API服务时，您的数据将会被传输给大模型语言厂商；如果您想了解这些数据将如何使用，您则需要查看这些第三方模型服务的隐私政策和服务条款。


## 更新日志

- **2024年5月5日，** 增加支持月之暗面模型.
- **2024年4月25日，** 免费key支持gpt-3.5-turbo、gpt-4，dall-e-4付费支持高并发且稳定.


## 特点
1. 支持国内大模型厂商智谱AI、零一万物、月之暗面等常见的大语言模型
2. 支持国外OpenAI系列主要模型，无需科学上网，国内环境直接可用，如：***GPT-4***, ***DALL-E-3*** 等。
3. 免费版密钥支持GPT-4、Dall-e-3，一天25次。（付费版API私密性和稳定性更高）
4. 与官方完全一致的接口标准，兼容各种软件/插件。
5. 支持流式响应。
6. 个人可以完全免费使用。

## 🚩注意事项

❗️*如果遇到无回复，报错等情况，可以查看 [KAPI服务可用性](http://43.133.38.250:3001/status/kapi)，确认服务状态是否正常，以帮助排查问题。*

❗️**免费API Key仅可用于个人非商业用途，教育，非营利性科研工作中。免费API Key严禁商用，严禁大规模训练商用模型！训练科研用模型请提前加群联系我们。**

❗️我们将不定期对被滥用的Key进行封禁，如发现自己的key被误封请通过微信群联系我们。

❗️我们的线上系统仅供个人评估测试使用，商用或面向大众可与我们联系私有部署提供专属无限制的APIKEY。

❗️免费共享API Key限制**25次请求/天/Key**调用频率（各模型调用次数总计25次）(更高更稳定的需求可以购买**KAPI付费版API**或**KAPI专属节点服务**)

## 免费使用

- **🚀[免费API Key](http://k.imiyoo.com)**
- 免费版支持gpt-3.5-turbo,gpt-4,dall-e-3。每天限制25次调用（24小时后刷新）。
- 我们会定期根据使用量进行相应的扩容，如果该项目对你有帮助，还请为我们点一个***Star***。如果遇到问题可以在Issues中反馈，我们会进行解答。
- 该API Key可用于对大语言模型服务进行路由和转发，只需要将base_url地址改为：`https://ai.imiyoo.com`。

## 付费版API服务
- 纯公益提供免费Key显然不是能持久运营下去的方案，所以我们引入付费API Key维持项目的日常开销，以促进项目的良性循环，还望大家理解。
- [大模型费用标准（持续更新）](https://apifox.com/apidoc/shared-f81e1fd6-279b-4314-9b4d-a5708355fb7e/doc-4282167)

1. 支持**更稳定更快速的GPT4/DallE3 API**，价格实惠。
2. 业界标准的计费策略，无官方返回Tokens利用tiktoken库准确计算Tokens，若官方返回Tokens用量计数则直接以官方为准。
3. 所有的接口（包括免费版本）都保证转发自模型厂商的官方接口，无额外中专，同时保证稳定性。

## 付费版专属节点
- 私有化部署，并提供所支持大模型厂商的专有APIKEY,支持更高的稳定性和私密性。


## 如何使用
- 🚀[领取免费API Key](http://k.imiyoo.com) 或 [共享兑换KAPI Key](https://apifox.com/apidoc/shared-f81e1fd6-279b-4314-9b4d-a5708355fb7e)
- KAPI大模型网关地址: `https://ai.imiyoo.com` (支持OpenAI系列模型国内中转)
- 可以替换OpenAI的API服务，只需要将服务地址改为：**https://ai.imiyoo.com** 即可使用，大部分插件和软件均支持修改。
- 遇到问题可以前往[KAPI Status](http://43.133.38.250:3001/status/kapi)查看所有接口服务可用性。

## 常见软件/插件使用方法

### **python openai官方库（使用AutoGPT，langchain等）**
请参考如下示例代码或[KAPI官方文档](https://apifox.com/apidoc/shared-f81e1fd6-279b-4314-9b4d-a5708355fb7e)

以下两种方式均支持访问使用，无须担心是否需要添加“/v1”后缀

```python
from openai import OpenAI

client = OpenAI(
    # defaults to os.environ.get("OPENAI_API_KEY")
    api_key="YOUR API KEY",
    base_url="https://ai.imiyoo.com"
)
```

```python
from openai import OpenAI

client = OpenAI(
    # defaults to os.environ.get("OPENAI_API_KEY")
    api_key="YOUR API KEY",
    base_url="https://ai.imiyoo.com/v1"
)
```

### 待补充（第三方软件或插件）
