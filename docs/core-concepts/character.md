---
sidebar_position: 2
---

# Character

Nomland 的 Character 允许您设置用户名，头像和其他个人资料。每一个用户都对应着一个 character，通过 character 可以分享评论或推荐，也可以回复等。每一个 Character 都有唯一的 id 及 handle。

此外，每一个 context 也被赋予了一个 character。此类特殊的社区 character 对于建立起一个社区形象非常有用。

## 所有权

一般来说 character 由最终用户所有且自行管理。

出于更好的用户体验，使用 dApp 创建的新的 character 可以根据需要替用户保管。但这种情况下应该允许用户认领回自己的 character，并且通过权限管理允许或取消 dApp 的授权。

dApp 可以根据需求请求 character 的权限。

## 权限管理

为了更好的用户体验，Nomland 未来会支持用户授予一部分代理操作的权力给指定的 dApp，或者别的 character。

个人 Character 可以授权特定 dApp 或其他 Character 发布、修改或删除内容。

社区 Character 是一类特殊的 Character，通过社区 Character 的授权操作可以实现对社区的一系列必要管理。例如：设置社区简介和 LOGO、管理社区拥有的 Curation 等。

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
