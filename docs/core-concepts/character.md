---
sidebar_position: 2
---

# Character

Nomland 的 Character 允许您设置用户名，头像和其他个人资料。每一个用户都对应着一个 character，通过 character 可以分享评论或推荐，也可以回复等。每一个 Character 都有唯一的 id 及 handle。

此外，每一个 context 也被赋予了一个 character。此类特殊的社区 character 对于建立起一个社区形象非常有用。


## 授权

为了更好的用户体验，Nomland 未来会支持用户授予一部分代理操作的权力给指定的 dApp，或者别的 character。

授权相关功能包括：

- 社区 Character 可以授权社区成员管理社区的名称，介绍，头像等。
- 个人 Character 可以授权特定 dApp 或其他 Character 发表内容。

## 数据格式定义

character 及其 metadata 的基本定义如下：

```typescript

interface CharacterMetadata {
    name?: string;
    avatars?: string[];
    bio?: string;
}

type Character = {
    handle: string;
    characterId: string;
    metadata: CharacterMetadata;
};

```
