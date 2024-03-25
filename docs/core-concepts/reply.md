---
sidebar_position:
---

# Reply

Reply 是指对 [Review](./review) 或 [Share](./share) 的回复。对 Share 的 Reply 会继承对应的 Context。

## 所有权

所有回复的数据所有权由发起回复的 Character 拥有。

## 数据结构

| 元素    | 是否必须 | 描述                                           | 示例                                     |
| ------- | -------- | ---------------------------------------------- | ---------------------------------------- |
| author  | 是       | 发起 Reply 的 [Character](./character)         | 如 Alice                                 |
| replyTo | 是       | Reply 指向的 Review 或 Share                   | 一串表示 review id 的字符串，如 `172-12` |
| Details | 是       | Reply 的详细信息，包括标题、正文、标签、附件。 |                                          |

特别说明，Reply 的实现基于了底层 Crossbell 协议的 Note，所以数据结构也继承了 Note 的数据结构。具体的结构定义参考 [Specification 小节](../nomexer-sdks/specification)。
