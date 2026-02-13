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

## .github resources

- .github/copilot-instructions.md - Copilot editing guidance for this repo
- .github/remote-index.md - Perchance tutorials and live/edit links for generators/plugins
- .github/plugin-index.json - catalog of Perchance plugins with snippets

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
