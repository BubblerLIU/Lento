---
title: 用 API+CheeryStudio 打造专属 AI 助手
description: 使用 CheeryStudio 接入 API ，创建个性化、可定制的 AI 助手
pubDatetime: 2025-11-18T19:00:00+08:00
featured: true
tags:
    - " AI"
    - " LLM"
---

这篇文章将介绍如何使用 CheeryStudio 软件通过 API 获取大模型服务，并搭建自己个性化的 AI 助手。

> API 是“应用程序编程接口”（Application Programming Interface）的简称。它是一组约定好的规则和接口，让不同的软件或服务之间可以相互通信、调用功能或交换数据。你可以把 API 想象成“服务员”：你（客户端）向服务员（API）点菜（发送请求），厨房（服务器）做菜（处理逻辑/数据），服务员把菜端给你（返回响应）。

## 获取 API

### 途径

大模型厂商除了在网页端提供对话服务，还提供 API 服务。通过 API ，我们可以把大模型直接接入到其它应用程序，甚至是我们自己编写的程序。获取 API 的方法有：

- 官方 API
- API 中转站

例如，我们可以访问 [Moonshot AI 开放平台](https://platform.moonshot.cn/docs/overview) 来获取 Kimi 大模型的 API 服务。

但是，API 服务通常都需要付费。有的大模型厂商会提供非常强劲的折扣，例如 [阿里云百炼](https://bailian.console.aliyun.com/) 的通义千问系列大模型，提供给用户 1M Token 的免费额度，通过学生认证还能获得 300 元代金券。通常，一次对话消耗的 Token 为几百到几千不等，产生的开销约为几厘到几分钱，因此 1M Token + 300 元代金券对于日常使用来说几乎花不完。

> Token 代表常见的字符序列，是大模型进行语言处理的基本单位。每个汉字使用的 Token 数目可能是不同的。例如，单个汉字"夔"可能会被分解为若干 Token 的组合，而像"中国"这样短且常见的短语则可能会使用单个 Token。

但是，一些国外的大模型，如 GPT 和 Gemini 系列，由于本身定价较高和汇率因素，其官方 API 服务对国内用户来说较为昂贵，而且其服务器在国内常常无法直接访问。API 中转站应运而生，它们以较低的价格和延迟向国内用户提供 API 中转服务，典型的代表如 [云雾 API](https://yunwu.ai/)。

### 操作方法

这里只介绍云雾 API 中转站的注册和使用，其他平台类似，且通常都有较完整的说明文档。

首先，我们要注册一个账号，这一步是平凡的。注册完成并登录，可以看到以下界面。

![云雾 API 控制台](https://gitee.com/lento_1_0/blog_pic_bed/raw/master/llm-1.png)



