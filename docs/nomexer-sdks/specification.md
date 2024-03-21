---
sidebar_position: 3
---
# Specification

<!-- TODO: code generated -->

``` Typescript
# Character
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

# Review

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

# Reply

interface Reply {
    character: Character; // 回复的人
    detail: NoteDetails; // 回复的内容
    idRepliedTo: string; // 回复对象的id
}

```