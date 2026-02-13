# Perchance Project Moss

A collection of Perchance generators, a text-to-image framework plugin.

## Repository layout

- generators/ - Perchance generators (HTML + list files)
- plugins/ - Perchance plugins used by generators
- characters/ - character prompt templates and profiles
- docs/ - miscellaneous notes and links
- .github/ - Copilot instructions and project indexes

## Generators

- AI Code Generator Moss
  - HTML: generators/ai-code-generator-moss/index.html
  - List: generators/ai-code-generator-moss/list.perchance
  - Live: https://perchance.org/ai-code-generator-moss
- AI Text Rewriter Moss
  - HTML: generators/ai-text-rewriter-moss/ai-text-rewriter-moss.html
  - List: generators/ai-text-rewriter-moss/ai-text-rewriter-moss.perchance
  - Live: https://perchance.org/ai-text-rewriter-moss
- AI Text Rewriter Moss NSFW
  - HTML: generators/ai-text-rewriter-moss-nsfw/ai-text-rewriter-moss-nsfw.html
  - List: generators/ai-text-rewriter-moss-nsfw/ai-text-rewriter-moss-nsfw.perchance
  - Live: https://perchance.org/ai-text-rewriter-moss-nsfw
  - Note: contains adult content. Handle with care.
- AI Text to Image Generator Moss
  - HTML: generators/ai-text-to-image-generator-moss/ai-text-to-image-generator-moss.html
  - List: generators/ai-text-to-image-generator-moss/ai-text-to-image-generator-moss.perchance
  - Live: https://perchance.org/ai-text-to-image-generator-moss

See .github/remote-index.md for additional live links and editing URLs.

## Plugins

- t2i-framework-plugin-moss
  - HTML: plugins/t2i-framework-plugin-moss/t2i-framework-plugin-moss.html
  - List: plugins/t2i-framework-plugin-moss/t2i-framework-plugin-moss.perchance
  - Live: https://perchance.org/t2i-framework-plugin-moss

The text-to-image generator uses the framework plugin (t2i-framework-plugin-v2) to generate the HTML interface from the list-side settings.

## Editing Perchance generators

- Keep HTML in the HTML editor file and list logic in the .perchance file.
- List variables are injected into HTML using [functionName()] and {variableName}.
- Avoid injecting raw JSON into script tags; use hidden elements or data attributes.
- If a generator uses t2i-framework-plugin-v2, edit the settings list instead of HTML.

## Characters

The characters/ folder contains character prompt templates and examples for AI character creation. These are plain markdown files and can be edited directly.

## Docs

- docs/other.md - external plugin and asset links used across the project

## License

No license specified.
