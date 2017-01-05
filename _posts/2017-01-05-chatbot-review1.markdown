---
title: Chatbot Toolsets Review
author: eBeam
layout: post
tags:
  - 人工智能
---

最近工作上的需要, 研究了一下市面上用来搭建聊天机器人的工具. 稍微总结了一下.

现在由于云平台的广泛使用, 搭建一个自娱自乐的聊天机器人是个非常简单的事情.
基本上各种产品都可以在10分钟搭出一个hello world出来, 由于西部世界这部美剧的播出. 聊天机器人的hello world变成了"It doesn't look like anything to me."

如果把聊天机器人也分为前端和后端来讲. 前端就是和用户交互的. 可以是微信公众号. 现在美国这边类似的就是Facebook Messenger. 一般稍微设一下crendential和webhook就可以了. 一些更友好的平台为了简化流程, 只需要你用Facebook账号authorization一下就可以做到一键发布(2个click). 值得提一句的是, Facebook Messenger的chatbot做出来之后, 本人作为admin用户可以测试, 但并不是对public公开的, 需要经审核.

下面重点讨论一下后端. 后端主要涉及几个概念/模块, 自然语言处理(NLP), 判断用户意图(intent), 还有故事线/剧本. 有的平台叫做flow, 有的叫做story. 按照WestWorld的叫法应该称为narration.

有一些后端几乎完全跳过了NLP这一层, 通过提示卡(quick response)的方法来跟用户交互, 这个被称为ping-pong conversation, 比较典型的一个产品叫chatfuel, 在我试用过产品里面属于性价比很高的chatbot平台. 其实互联网产品, 有一个大类就是让用户提交表单, 表单的一个好处是比较well-defined, 可以逐一validate, 缺点就是比较繁琐. 这是聊天机器人的优势所在, 如果足够"聪明"的话, 你两三句话的信息可能需要表单里面填十个空. 而且加上语音识别模块. 是不是一下子优势就体现出来了?

比较智能的平台一般都可以同过监督学习来训练对于用户intent的判断. 如果把平台作为一个mininal的接口来看的话, 可以想象成输入是语音或文字, 而输出是对于用户意图的一个判断. 这个判断是通过人工加标签的方法训练出来的. 而有了用户意图的判断, 然后用这个用户意图来设计flow

整体来说, chatbot/AI助理很大程度上一些大的厂商在进行布局, Google和Facebook分别收购了api.ai和wit.ai chatbot平台,  这两个平台我都稍微试用了一下. 有一些初步的心得, 会在下一篇文章里面更详细的阐述一下.
