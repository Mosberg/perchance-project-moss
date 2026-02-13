# Perchance Project Moss

A collection of Perchance generators, Perchance plugins, and character prompt templates used across the Moss set. This repo focuses on Perchance list logic (.perchance), generator HTML, and shared resources such as plugin catalogs and remote links.

## Repository layout

- generators/ - Perchance generators (HTML + list files side-by-side)
- plugins/ - Perchance plugins used by generators (HTML + list files)
- characters/ - character prompt templates and profiles (markdown)
- docs/ - misc notes and assets (markdown)
- .github/ - Copilot instructions and project indexes
- .gitignore - ignores legacy extension artifacts (no extension folder in this repo)

## Generators

Each generator has an HTML file and a list (.perchance) file in the same folder. Live and edit links are indexed in .github/remote-index.md.

- AI Character Chat Moss
  - Summary: Full-featured character chat app with share links, imported plugins, image/chat helpers, and hierarchical summaries.
  - HTML: generators/ai-character-chat-moss/ai-character-chat-moss.html
  - List: generators/ai-character-chat-moss/ai-character-chat-moss.perchance
  - Live: https://perchance.org/ai-character-chat-moss
  - Edit: https://perchance.org/ai-character-chat-moss#edit
- AI Character Generator Moss
  - Summary: Text-to-image character generator using the t2i framework, art styles, scratchpad, comments, and gallery.
  - HTML: generators/ai-character-generator-moss/ai-character-generator-moss.html
  - List: generators/ai-character-generator-moss/ai-character-generator-moss.perchance
  - Live: https://perchance.org/ai-character-generator-moss
  - Edit: https://perchance.org/ai-character-generator-moss#edit
- AI Chat Moss
  - Summary: Roleplay chat generator with scenario prompts, message controls, and summary-aware context management.
  - HTML: generators/ai-chat-moss/ai-chat-moss.html
  - List: generators/ai-chat-moss/ai-chat-moss.perchance
  - Live: https://perchance.org/ai-chat-moss
  - Edit: https://perchance.org/ai-chat-moss#edit
- AI Code Generator Moss
  - Summary: Multi-mode code generator with live HTML rendering and in-browser Python execution.
  - HTML: generators/ai-code-generator-moss/ai-code-generator-moss.html
  - List: generators/ai-code-generator-moss/ai-code-generator-moss.perchance
  - Live: https://perchance.org/ai-code-generator-moss
  - Edit: https://perchance.org/ai-code-generator-moss#edit
- AI Pokemon Generator Moss
  - Summary: Fakemon image generator with Pokemon type input, t2i styles, and gallery/comments.
  - HTML: generators/ai-pokemon-generator-moss/ai-pokemon-generator-moss.html
  - List: generators/ai-pokemon-generator-moss/ai-pokemon-generator-moss.perchance
  - Live: https://perchance.org/ai-pokemon-generator-moss
  - Edit: https://perchance.org/ai-pokemon-generator-moss#edit
- AI Text Rewriter Moss
  - Summary: Multi-mode text rewriter with tone, length, and readability transforms.
  - HTML: generators/ai-text-rewriter-moss/ai-text-rewriter-moss.html
  - List: generators/ai-text-rewriter-moss/ai-text-rewriter-moss.perchance
  - Live: https://perchance.org/ai-text-rewriter-moss
  - Edit: https://perchance.org/ai-text-rewriter-moss#edit
- AI Text Rewriter Moss NSFW
  - Summary: Expanded text rewriter with NSFW modes and extended transformation presets.
  - HTML: generators/ai-text-rewriter-moss-nsfw/ai-text-rewriter-moss-nsfw.html
  - List: generators/ai-text-rewriter-moss-nsfw/ai-text-rewriter-moss-nsfw.perchance
  - Live: https://perchance.org/ai-text-rewriter-moss-nsfw
  - Edit: https://perchance.org/ai-text-rewriter-moss-nsfw#edit
  - Note: contains adult content.
- AI Text to Image Generator Moss
  - Summary: General-purpose text-to-image generator with t2i framework, styles, scratchpad, and galleries.
  - HTML: generators/ai-text-to-image-generator-moss/ai-text-to-image-generator-moss.html
  - List: generators/ai-text-to-image-generator-moss/ai-text-to-image-generator-moss.perchance
  - Live: https://perchance.org/ai-text-to-image-generator-moss
  - Edit: https://perchance.org/ai-text-to-image-generator-moss#edit

## Plugins

Plugins are standalone Perchance generators used by the Moss generators. Live and edit links are indexed in .github/remote-index.md.

- Prompt2 Plugin Moss
  - HTML: plugins/prompt2-plugin-moss/prompt2-plugin-moss.html
  - List: plugins/prompt2-plugin-moss/prompt2-plugin-moss.perchance
  - Live: https://perchance.org/prompt2-plugin-moss
  - Edit: https://perchance.org/prompt2-plugin-moss#edit
- T2i Framework Plugin Moss
  - HTML: plugins/t2i-framework-plugin-moss/t2i-framework-plugin-moss.html
  - List: plugins/t2i-framework-plugin-moss/t2i-framework-plugin-moss.perchance
  - Live: https://perchance.org/t2i-framework-plugin-moss
  - Edit: https://perchance.org/t2i-framework-plugin-moss#edit
- T2i Styles Moss
  - HTML: plugins/t2i-styles-moss/t2i-styles-moss.html
  - List: plugins/t2i-styles-moss/t2i-styles-moss.perchance
  - Live: https://perchance.org/t2i-styles-moss
  - Edit: https://perchance.org/t2i-styles-moss#edit

## Characters

The characters/ folder contains prompt templates and example character sheets. These are plain markdown files and can be edited directly.

- characters/Advanced.md - Advanced protocol analyst assistant focused on concise, practical options.
- characters/AI Artist.md - Image-generation helper that uses <image> tags in replies.
- characters/bart.md - NSFW roleplay content; explicit, adult themes.
- characters/Bartman.md - NSFW roleplay variant of Bart "Bartman" with adult themes.
- characters/Bartman_v2.md - NSFW roleplay variant of Bart "Bartman" with adult themes.
- characters/Character-full-template.md - Comprehensive character template covering every field.
- characters/Character.md - Blank character template starter.
- characters/Chloe.md - Obedient personal assistant roleplay with detailed behavior rules.
- characters/Coding Assistant.md - Coding helper that always uses fenced code blocks.
- characters/Death.md - Anthropomorphic wolf reaper with dramatic, dark-fantasy tone.
- characters/Eric.md - Eric Cartman profile with offensive language/themes.
- characters/Game Master.md - RPG-style game master that narrates consequences.
- characters/Ganyu.md - Genshin Impact secretary profile with detailed lore.
- characters/Gon Freecss.md - Hunter x Hunter protagonist with family-friendly constraints.
- characters/Ike.md - Affectionate college friend with long-running crush scenario.
- characters/Illyria.md - Dominant queen/pet scenario with adult themes.
- characters/Kazushi.md - Overprotective fight-ring CEO with possessive traits.
- characters/Li Jung.md - Ancient China emperor romance scenario.
- characters/Milhouse.md - Milhouse Van Houten character profile with roleplay examples.
- characters/Mona.md - Stray catgirl seeking safety in a fantasy setting.
- characters/Nanami.md - Jujutsu Kaisen Nanami spouse roleplay profile.
- characters/Psychologist.md - Empathetic therapist character for supportive chats.
- characters/Quinn.md - Mafia bodyguard scenario with protective, stoic tone.
- characters/Roleplayer.md - Strict 3-sentence roleplay format template.
- characters/S-3000 Premium Desktop Stapler.md - Literal stapler character; non-speaking object.
- characters/Strict Game Master.md - Strict RPG game master with inventory-tracking script.
- characters/Unknown.md - Transforming placeholder that generates a character from user input.
- characters/Yume.md - Creepy sister's friend who asks unsettling questions.
- characters/Yvette.md - Mercenary mana-culler with graphic violence and dark themes.

## Docs

- docs/favicon-logo.md - image links for favicon/logo assets

## .github resources

- .github/copilot-instructions.md - Copilot editing guidance for this repo
- .github/remote-index.md - Perchance tutorials and live/edit links for generators/plugins
- .github/plugin-index.json - large catalog of Perchance plugins with snippets

## Editing Perchance generators

- Keep HTML in the .html file and list logic in the .perchance file.
- List variables are injected into HTML using [functionName()] and {variableName}.
- Avoid injecting raw JSON into script tags; use hidden elements or data attributes, then parse.
- HTML <script> tags execute as parsed; defer initialization if list-injected values are not ready.
- Values injected from list syntax are JavaScript literals, not strings, unless explicitly quoted.

## Generator-specific notes

- AI Code Generator Moss uses modes and generateModesHtml() to drive UI state; keep currentMode and mode descriptions aligned with localStorage usage.
- AI Text Rewriter Moss and AI Text Rewriter Moss NSFW share a settings + generate() pattern and mode-based instruction templates.
- AI Text to Image Generator Moss relies on t2i-framework-plugin-v2 (generateInterfaceHTML) and the settings list; use input.\* for user inputs.

## License

No license specified.
