---
sidebar_position: 3
---

# Review

Review 是协议中的核心概念。每一个 Review 由某个 Character 发起，针对某个 Entity，包含一些的 Detail，在某个 Context 中发生。


## 数据结构定义
每一个 Review 包含以下几个元素：
- Character
    - Review 的发起者。参考 [Character](./character)
- Context
    - 任何 Review 都有 context，这个 context 可能是社区，也可能是某个应用。每个 context 都会被赋予一个 Character，有唯一的 id，可选择性拥有昵称头像简介等其他个性化信息。
- Entity
    - 分享评论推荐的具体内容，对应 [Entity](./entity)
- Details
    - Review 的 details，包含标题，内容，图片，标签等。
- Collector：Review 可能并不是由本人提交到 Nomland Network 中，而是由 Collector 提交的。

具体的结构定义如下：

```typescript
interface Review {
		character: Character; // the one who shares something.
		entity: Entity; // the object to share, e.g. an article/a cafe...
    context: Character; // the context where the sharing happens
    details: NoteDetails; // "the reason that sharer proposes along with the sharing"
		collector: string; // who collects this piece of sharing: ethereum address
}

interface NoteDetails {
    content?: string;
    attachments?: Attachment[];
    date_published?: string;
    tags?: string[];
    title?: string;
    sources?: string[];
    external_url?: string;
    content_warning?: "nsfw" | "sensitive" | "spoiler";
    rawContent?: string[];
}

interface Attachment {
    /**
     * The name of this attachment.
     */
    name?: string;
    /**
     * The plain content of this attachment.
     */
    content?: string;
    /**
     * The mime type of the `content`.
     */
    mime_type?: string;
    /**
     * The size of the `content` in bytes.
     */
    size_in_bytes?: number;
    /**
     * The alternate text (description) of this attachment.
     * This is used for accessibility or is displayed when the source is not available.
     */
    alt?: string;
    /**
     * The width of this attachment, in pixels.
     */
    width?: number;
    /**
     * The height of this attachment, in pixels.
     */
    height?: number;
}
```
