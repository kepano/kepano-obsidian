# Obsidian Vault Template

## Origin & Philosophy

I wanted to get started with Obsidian and discovered Steph Ango's [blog](https://stephango.com/vault) and Karlos' [video](https://www.youtube.com/watch?v=Dq3R3uS0sQ4&t=789s). I found the philosophy behind it fascinating. However, I found the original vault was a bit too complex and overwhelming for a beginner, at least for me.

This repository is a **simplified version** that I customized to fit my preferences (e.g., folder structure, snake_case naming). I highly recommend reading the original blog post and watching the video to understand the "Why". You can start with the original or use this simplified version as a lighter starting point.

## Core Concepts

This vault is designed to avoid rigid folder structures. Instead, it relies on **Links** to organize everything.

1.  **Everything is a Link**: Whether it's a Category (like `[[notes]]`), a Topic (like `[[ai]]`), or a specific concept (like `[[deep_work]]`), they are all just links to files in the `references/` folder.
2.  **Properties**:
    *   **Category**: Think of this as a "System Tag". It defines the *type* of the note (e.g., Is it a daily journal? A clipped article?).
    *   **Topic**: Defines the *subject* of the note.
3.  **References**: All these links point to files in `references/`. When you open `[[ai]]`, you don't just see a blank page; you see a dynamically generated table of every note you've ever tagged with "ai".

## Vault Structure

Here is a quick overview of the folders and what they do:

```text
.
├── files/              # THE POOL. Almost all your notes live here flatly.
├── journals/           # Yearly aggregations (e.g., 2025.md).
├── references/         # THE INDEX. Contains the files for topics and categories.
├── templates/          # Templates for creating new notes.
│   ├── bases/          # Defines the "Views" (tables) used in references.
│   ├── daily_template  # For daily streams of thought.
│   ├── note_template   # For standard atomic notes.
│   ├── post_template   # For drafting content to publish.
│   └── clipping_template # For articles/content saved from the web.
└── attachments/        # Drag & drop images here; they auto-save to this folder.
```

## How to continue

You can download this repository, open it with Obsidian, and click around the links to experience the flexibility of this system.

I highly recommend watching the video mentioned above. It provides a step-by-step walkthrough that is easy to follow and covers the philosophy from the blog, which can be a bit brief on its own. After watching, come back and explore this vault again—I believe you'll gain a deeper understanding of how the components work together and how to effectively create new notes, topics, and categories.

