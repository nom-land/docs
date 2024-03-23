---
sidebar_position: 4
---

# Review

Review 是协议中的核心概念。每一个 Review 由某个 Character 发起，针对某个 Entity，包含一些的 Detail，在某个 Context 中发生。

## 所有权

所有 Review 的数据所有权由发起 Review 的 Character 拥有。

## 数据结构

每一个 Review 包含以下几个元素：

| 元素      | 描述                                                          | 示例                     |
| --------- | ------------------------------------------------------------- | ------------------------ |
| Character | Review 的发起者。参考 [Character](./character)                | 如 Alice                 |
| Context   | Review 发生的上下文。                                         | Book Fans Community      |
| Entity    | 分享评论推荐的具体内容，对应 [Entity](./entity)               | 一本书                   |
| Details   | Review 的详细信息。                                           | 标题，内容，标签，图片等 |
| Collector | Review 可能由 Collector 提交到 Nomland Network 中，而非本人。 | 一个以太坊地址           |

特别说明，Review 的实现基于了底层 Crossbell 协议的 Note，所以数据结构也继承了 Note 的数据结构。具体的结构定义参考 [Specification 小节](../nomexer-sdks/specification)。
