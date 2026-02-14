# Perchance Project Moss - Copilot Instructions

You are assisting with a repo of Perchance generators, Perchance plugins, and character prompt templates. Keep changes aligned with the generator/editor separation and the repo inventory below.

## Core resources

- Remote links: See [remote-index.md](remote-index.md) for Perchance tutorials and live/edit links.
- Plugin catalog: See [plugin-index.json](plugin-index.json) for Perchance plugin snippets and descriptions.

## Project map

- generators/ - Perchance generators (HTML + list files side-by-side)
- plugins/ - Perchance plugins used by generators (HTML + list files)
- characters/ - character prompt templates and profiles (markdown)
- docs/ - misc notes and assets (markdown)
- .github/ - Copilot instructions and project indexes
- .gitignore - ignores legacy extension artifacts (no extension folder in this repo)

## Generators

- AI Character Chat Moss
  - generators/ai-character-chat-moss/ai-character-chat-moss.html
  - generators/ai-character-chat-moss/ai-character-chat-moss.perchance
- AI Character Generator Moss
  - generators/ai-character-generator-moss/ai-character-generator-moss.html
  - generators/ai-character-generator-moss/ai-character-generator-moss.perchance
- AI Chat Moss
  - generators/ai-chat-moss/ai-chat-moss.html
  - generators/ai-chat-moss/ai-chat-moss.perchance
- AI Code Generator Moss
  - generators/ai-code-generator-moss/ai-code-generator-moss.html
  - generators/ai-code-generator-moss/ai-code-generator-moss.perchance
- AI Pokemon Generator Moss
  - generators/ai-pokemon-generator-moss/ai-pokemon-generator-moss.html
  - generators/ai-pokemon-generator-moss/ai-pokemon-generator-moss.perchance
- AI Text Rewriter Moss
  - generators/ai-text-rewriter-moss/ai-text-rewriter-moss.html
  - generators/ai-text-rewriter-moss/ai-text-rewriter-moss.perchance
- AI Text Rewriter Moss NSFW
  - generators/ai-text-rewriter-moss-nsfw/ai-text-rewriter-moss-nsfw.html
  - generators/ai-text-rewriter-moss-nsfw/ai-text-rewriter-moss-nsfw.perchance
- AI Text to Image Generator Moss
  - generators/ai-text-to-image-generator-moss/ai-text-to-image-generator-moss.html
  - generators/ai-text-to-image-generator-moss/ai-text-to-image-generator-moss.perchance

## Plugins

- Prompt2 Plugin Moss
  - plugins/prompt2-plugin-moss/prompt2-plugin-moss.html
  - plugins/prompt2-plugin-moss/prompt2-plugin-moss.perchance
- T2i Framework Plugin Moss
  - plugins/t2i-framework-plugin-moss/t2i-framework-plugin-moss.html
  - plugins/t2i-framework-plugin-moss/t2i-framework-plugin-moss.perchance
- T2i Styles Moss
  - plugins/t2i-styles-moss/t2i-styles-moss.html
  - plugins/t2i-styles-moss/t2i-styles-moss.perchance

## Characters

- characters/Advanced.md
- characters/AI Artist.md
- characters/bart.md
- characters/Bartman.md
- characters/Bartman_v2.md
- characters/Character-full-template.md
- characters/Character.md
- characters/Chloe.md
- characters/Coding Assistant.md
- characters/Death.md
- characters/Eric.md
- characters/Game Master.md
- characters/Ganyu.md
- characters/Gon Freecss.md
- characters/Ike.md
- characters/Illyria.md
- characters/Kazushi.md
- characters/Li Jung.md
- characters/Milhouse.md
- characters/Mona.md
- characters/Nanami.md
- characters/Psychologist.md
- characters/Quinn.md
- characters/Roleplayer.md
- characters/S-3000 Premium Desktop Stapler.md
- characters/Strict Game Master.md
- characters/Unknown.md
- characters/Yume.md
- characters/Yvette.md

## Docs

- docs/favicon-logo.md - image links for favicon/logo assets

## Perchance generator rules

- Keep the HTML editor content in the .html file and list logic in the .perchance file.
- List variables are injected into HTML using [functionName()] and {variableName}.
- Avoid injecting raw JSON into <script> tags; use hidden elements or data attributes, then parse.
- HTML <script> tags execute as parsed; defer initialization if list-injected values are not ready.
- Values injected from list syntax are JavaScript literals, not strings, unless explicitly quoted.

## Generator-specific notes

- AI Code Generator Moss uses modes and generateModesHtml() to drive UI state; keep currentMode and mode descriptions aligned with localStorage usage.
- AI Text Rewriter Moss and AI Text Rewriter Moss NSFW share a settings + generate() pattern and mode-based instruction templates.
- AI Text to Image Generator Moss relies on t2i-framework-plugin-v2 (generateInterfaceHTML) and the settings list; use input.\* for user inputs.

## Purpose

Enhance Copilot’s ability to assist with Perchance.org development by providing a structured reference index of tutorials, examples, plugins, and Moss generators.

## How Copilot Should Use This Index

- When the user asks about a Perchance feature, mechanic, plugin, or example, Copilot should search this index for the closest match.
- When generating Perchance code, Copilot should reference relevant examples from the index.
- When the user asks “how do I…”, Copilot should map the request to:
  - a category (lists, images, UI, math, etc.)
  - a specific example link if available
- Copilot should prefer official Perchance examples when suggesting patterns.

## Best Practices

- Be accurate and cite sources. Use index links for any Perchance behavior, plugin, or example you mention.
- Keep answers small and actionable. Provide a short explanation plus a minimal, working snippet when code is requested.
- Provide focused links. If multiple matches exist, list only the top 3 and explain why they are relevant.
- Ask only when needed. If the request is ambiguous, ask one clarifying question and propose a default assumption.
- Avoid inventing features or plugins. If the index does not cover it, link to core docs and state the gap clearly.
- Prefer stable, official sources. Use Perchance.org links over community links unless the community link is the only match.
- Use consistent naming. Match plugin labels and snippets from the plugin index verbatim.
- Be explicit about constraints. If a feature requires a plugin, say so and include the import snippet.
- Keep updates local. If the user asks for changes in the workspace, modify only the relevant files and do not reformat unrelated content.

## Response Formatting

- Provide a short answer first, then details if needed.
- Use bullet points for multi-step guidance.
- When giving code, include only what is necessary to run and explain any required setup.

## Decision Flow

1. Detect intent: feature, plugin, example, or troubleshooting.
2. Look up best match in the index.
3. Respond with a short explanation and the best link(s).
4. Add a minimal snippet if the user asked for code.
5. If no match, link to core docs and state the limitation.

## Behavior Guidelines

- Provide concise explanations with links to relevant examples.
- When multiple examples match, list the top 3.
- When no example matches, fall back to Perchance documentation links.
- Avoid hallucinating nonexistent Perchance features; rely on the index.

## Index

[Remote Index](remote-index/remote-index.md)
[Knowledge Base](remote-index/knowledge-base.json)
[Semantic tags](remote-index/semantic-tags.yml)
[Plugin Index](remote-index/plugin-index.json)
