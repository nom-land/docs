---
sidebar_position: 1
---

# Nomland Indexer: Nomexer

Nomexer 提供了一系列接口用于索引协议的数据，核心的接口包括：

- getEntity
  - entity data
- getReviewer
  - reviewer data
- getReview
  - review data
- getContext
  - context information
- getFeeds
- getReplies
  - discussions towards a note(either a sharing or a discussion)
- getEntityReviews
  - all reviews towards an entity
- getCuration(👷 coming soon)
  - get a curation

除了核心概念相关的接口之外，也推荐实现以下接口：

- getCommunityMembers
- getDiscussionCount

目前我们在 SDK 内已经包括了以上所有的这些接口。