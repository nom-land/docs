---
sidebar_position: 3
---

# Community

Nomland 非常在意分享发生的场景，协议里 [Share](./share) 会记录发生的场景 context，大多数时候 context 会对应某一个 Community。
每一个 Community 都有唯一的 id 及 handle。
如果有一些 dApp 不打算记录场景，则应该把该 dApp 视作一个独特的场景，创建一个专门的 Community 作为内容发生的场景。

作为去中心的分享协议，Nomland 协议本身不会进行内容治理。日常内容治理应由 Community 自行管理。

## 所有权

一般来说，所有 Community 归创建人所有。

和 character 一样，出于更好的用户体验，使用 dApp 创建的新的 community 可以根据需要由应用代管。但这种情况下应该允许用户认领回自己创建的 community ，并且通过权限管理允许或取消 dApp 的授权。

dApp 可以根据需求请求 community 的权限。

## 权限管理

为了更好的用户体验，Nomland 未来会支持用户授予一部分代理操作的权力给指定的 character。
通过 community 授权操作可以实现对社区的一系列必要管理。例如：设置社区简介和 LOGO、管理 community 拥有的 Curation、社区[内容治理](./content-governance)等。

## 数据格式定义

具体的结构定义参考 [Specification 小节](../nomexer-sdks/specification)。
