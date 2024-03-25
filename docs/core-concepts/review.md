---
sidebar_position: 4
---

# Review

## 定义

Review 是由某个 character 针对某个 Entity 发表的评论，可以对 Review 回复（Reply）。

## 所有权

所有 Review 的数据所有权由发起 Review 的 Character 拥有。对 Review 回复的 Reply 数据所有权属于 Reply 的作者。

## 数据结构

每一个 Review 包含以下几个元素：

| 元素      | 是否必须 | 描述                                                             | 示例                       |
| --------- | -------- | ---------------------------------------------------------------- | -------------------------- |
| Author    | 是       | Review 的作者，对应一个 character。参考 [Character](./character) | 如 Alice                   |
| Entity    | 是       | Review 的对象，对应 [Entity](./entity)                           | 如一篇文章                 |
| Details   | 是       | Review 的详细信息，包括标题、正文、标签、附件。                  | 如一篇富文本评论文章及标签 |
| Collector | 否       | 帮助 Review 被协议收录的贡献者，一般也对应为一个 Character。     | 如 Bob                     |

特别说明，Review 的实现基于了底层 Crossbell 协议的 Note，所以数据结构也继承了 Note 的数据结构。具体的结构定义参考 [Specification 小节](../nomexer-sdks/specification)。
