---
sidebar_position: 4
---

# Reply

除了 Review 外，基于 Review 的回复也应该被记录，不仅因为这体现了Review 本身的价值，也是因为本质上来说，基于 Review 的讨论客观上也是对原本分享内容的再次分享。每一次 reply 的定义如下：
- Character: 回复的人
- detail：回复的细节
- idRepliedTo：具体回复的 note 的 id

```typescript
interface Reply {
    character: Character; // 回复的人
    detail: NoteDetails; // 回复的内容
    idRepliedTo: string; // 回复对象的id
}
```