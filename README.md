# Perchance Project Moss

A collection of Perchance generators, a text-to-image framework plugin, and a VS Code extension that adds Perchance language support and utilities.

## Repository layout

- generators/ - Perchance generators (HTML + list files)
- plugins/ - Perchance plugins used by generators
- extension/ - VS Code extension for Perchance language support
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

## VS Code extension

The extension in extension/ provides:

- Perchance language registration for .perchance and .prch
- Formatting and diagnostics for common list errors
- Commands for plugin insertion, generator creation, and list folding
- Snippets for Perchance lists and imports

Key files:

- extension/extension.js - extension logic
- extension/package.json - contribution points and commands
- extension/data/plugins.json - plugin catalog used by the Manage Plugins command
- extension/data/templates.json - generator templates

### Extension development

1. Open extension/ in VS Code.
2. Install dependencies:

```bash
npm install
```

3. Run the extension with the VS Code debugger (Run and Debug) or press F5.
4. Lint or test from the extension folder:

```bash
npm run lint
npm test
```

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
