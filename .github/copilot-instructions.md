# Perchance Project Moss - Copilot Instructions

You are assisting with a mixed repo that includes Perchance generators, a Perchance plugin, and a VS Code extension. Use the resources in this folder and keep changes aligned with the generator/editor separation.

## Core Resources

- Remote links: See [remote-index.md](remote-index.md) for Perchance tutorials, docs, and live generator links.
- Plugin catalog: See [plugin-index.json](plugin-index.json) for snippets and descriptions.

## Project Map

- Generators live under `generators/` with HTML and list files side-by-side.
- Plugin sources live under `plugins/` and include both HTML and list logic.
- VS Code extension lives under `extension/`.
- Character prompt templates live under `characters/`.

## Perchance Generator Rules

- Keep the HTML editor content in the `*.html` file and list logic in the `*.perchance` file.
- Do not inject raw JSON into `<script>` tags. Use hidden elements or data attributes, then parse.
- HTML `<script>` tags execute as parsed; defer initialization if list-injected values are not ready.
- Values injected from list syntax are JavaScript literals, not strings, unless explicitly quoted.

## Generator-Specific Notes

- `ai-code-generator-moss` uses `modes` and `generateModesHtml()` to drive UI state; keep `currentMode` and mode descriptions in sync with localStorage usage.
- `ai-text-rewriter-moss` and `ai-text-rewriter-moss-nsfw` share a common pattern of `settings` + `generate()` and mode-based instruction templates.
- `ai-text-to-image-generator-moss` relies on `t2i-framework-plugin-v2` (`generateInterfaceHTML`) and the `settings` list. Use the `input.*` namespace for user inputs.

## t2i Framework Plugin Notes

- The framework constructs the full HTML UI from a `settings` list. Ensure any changes remain backward-compatible unless a new version is introduced.
- User inputs are exposed under `window.input` and have optional `visible()`, `remember`, and `parseVariables` behavior.
- The plugin handles share links, galleries, and comments. Avoid breaking global hooks like `___userSettings746291937` and `___selectElChangeEvent746291937`.

## VS Code Extension Notes

- Extension entry point: `extension/extension.js`. Uses VS Code APIs for diagnostics, formatting, code actions, and commands.
- Plugin data and templates are loaded from `extension/data/*.json`.
- Do not add new commands without updating `extension/package.json` contributions.

## Common Patterns

### Pattern: Select Mode Injection

```html
<select id="currentModeEl" onchange="currentMode=this.value; localStorage.currentMode=this.value;">
  [generateModesHtml()]
</select>
```

```lua
generateModesHtml() =>
  return modes.selectAll.map(m => `<option value="${m.getName}">${m.label}</option>`).join("");
```

### Pattern: Hidden Select for Data Transfer

```html
<select id="modeOptionsTemplate" style="display: none">
  [generateModesHtml()]
</select>
<script>
  const modesData = Array.from(modeOptionsTemplate.options).map((option) => {
    return { name: option.value, label: option.textContent };
  });
</script>
```

## Debugging Tips

- Check browser console for HTML/JS errors first.
- If list values are missing, verify the list function exists and returns the right type.
- Use a small timeout to delay DOM wiring when injected values are needed.
- Keep Perchance list indentation at 2 spaces.

## Reference Links

- Perchance tutorial: https://perchance.org/tutorial
- Perchance advanced tutorial: https://perchance.org/advanced-tutorial
- Perchance plugins: https://perchance.org/plugins
- Perchance FAQ: https://perchance.org/perchance-faq
- Perchance known bugs: https://perchance.org/known-bugs
- Perchance generators: https://perchance.org/generators
