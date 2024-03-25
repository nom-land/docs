---
sidebar_position: 5
---

# Share

## 定义

Share 是协议中的核心概念，记录某个 Character 把协议中的某个内容（Entity、Review、Reply、Character、Community、Curation）分享到某个场景（Context）的行为。
Share 也可以被回复（Reply），并且针对 Share 的 Reply 会继承同一个 Context。

## 所有权

数据所有权由发起 Share 的 Character 拥有。对 Share 回复的 Reply 数据所有权属于 Reply 的作者。

## 数据结构

每一个 Share 包含以下几个元素：

| 元素      | 是否必须 | 描述                                                                                                                                                    | 示例                       |
| --------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------- |
| Author    | 是       | Share 的作者，分享人，对应一个 character。参考 [Character](./character)                                                                                 | 如 Alice                   |
| Context   | 否       | Share 对应的场景                                                                                                                                        | 例如某个 Community         |
| Item      | 是       | Share 的对象，对应 [Entity](./entity)、[Review](./review)、[Reply](./reply)、[Character](./character)、[Community](./community)、[Curation](./curation) | 如一篇 review              |
| Details   | 是       | Share 的详细信息，包括标题、正文、标签、附件                                                                                                            | 如一篇富文本评论文章及标签 |
| Collector | 否       | 帮助 Share 被协议收录的贡献者，一般也对应为一个 Character。                                                                                             | 如 Bob                     |

具体的结构定义参考 [Specification 小节](../nomexer-sdks/specification)。
