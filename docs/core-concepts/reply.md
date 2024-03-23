---
sidebar_position: 5
---

# Reply

除了 Review 外，基于 Review 的回复也应该被记录，不仅因为这体现了 Review 本身的价值，也是因为本质上来说，基于 Review 的讨论客观上也是对原本分享内容的再次分享。

## 所有权

所有回复的数据所有权由发起回复的 Character 拥有。

## 数据结构

| 元素        | 描述                           | 示例                          |
|-------------|-------------------------------|------------------------------|
| Character   | 发起 Reply 的人                | 如 Alice                     |
| Review      | Reply 指向的 Review            | 一串表示 review id 的字符串，如 ``172-12`` |
| Details     | Reply 的详细信息               | 标题，内容，标签，图片等       |



具体的结构定义参考 [Specification 小节](../nomexer-sdks/specification)。
