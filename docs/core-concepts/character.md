---
sidebar_position: 2
---

# Character

Character 是 Nomland 协议中的参与者，每一个用户都对应着一个 character，通过 character 参与 Review、Share、Reply 等。
每一个 character 都有唯一的 id 及 handle。
Character 可以设置用户名，头像和其他个人资料。

## 所有权

一般来说 character 由最终用户所有且自行管理。

出于更好的用户体验，使用 dApp 创建的新的 character 可以根据需要替用户保管。但这种情况下应该允许用户认领回自己的 character，并且通过权限管理允许或取消 dApp 的授权。

dApp 可以根据需求请求 character 的权限。

## 权限管理

为了更好的用户体验，Nomland 未来会支持用户授予一部分代理操作的权力给指定的 dApp，或者别的 character。

Character 可以授权特定 dApp 或其他 Character 发布、修改或删除内容。

所有关于 character 的授权都可以对针不同的操作对不同的人授予权限。

## 数据格式定义

具体的结构定义参考 [Specification 小节](../nomexer-sdks/specification)。
