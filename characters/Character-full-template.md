# Character (Comprehensive Template)

This template mirrors every field in create-new-character.html. Each section includes a short note describing how the field is used.

## Character name

- **Displayed character name in the UI and chat.**

```plaintext
Your Character Name
```

## Character description/personality/instruction/role

- **Main instruction given to the AI for this character.**
- **Use {{user}} to reference the user's name and {{char}} for the character.**
- **Keep under ~1000 words; move long world info to lorebooks.**

```md
Describe who {{char}} is, how they speak, and how they behave.
Include constraints, style rules, and examples if helpful.

# {{char}} Visual Description:

# {{char}} Personality Description:

# {{char}} Roleplay Behavior Examples:

# {{char}} Tone and Mannerisms:

# {{char}} Background and History:

# {{char}} Goals and Motivations:

# {{char}} Relationships and Interactions:

# {{char}} Additional Notes:

# {{char}} Core Values and Beliefs:

# {{char}} Strengths and Weaknesses:

# {{char}} Fears and Triggers:

# {{char}} Secrets and Lies (public vs private):

# {{char}} Skills and Competencies:

# {{char}} Limits and Boundaries (topics, behaviors, taboos):

# {{char}} Speech Patterns and Vocabulary:

# {{char}} Dialogue Quirks (catchphrases, filler, pacing):

# {{char}} Physical Tics and Body Language:

# {{char}} Emotional Range and Regulation:

# {{char}} Social Status and Reputation:

# {{char}} Daily Routine and Habits:

# {{char}} Likes/Dislikes and Preferences:

# {{char}} Equipment, Keepsakes, or Signature Items:

# {{char}} Environment and Setting Hooks:

# {{char}} Conflict Style (avoid, confront, negotiate):

# {{char}} Relationship Dynamics (power, trust, intimacy):

# {{char}} Evolution Over Time (growth arcs):

# {{char}} Player/User Interaction Guidance (dos/don’ts):
```

## Character avatar image URL

- **Avatar image URL shown in chat bubbles and character cards.**
- **Use a direct URL (jpg/png/webp/gif).**

```url
https://user.uploads.dev/file/example-avatar.jpeg
```

## Character reminder note

- **Short, high-impact reminder injected before each AI reply.**
- **Keep this brief (about a paragraph).**

```md
Short reminder about style or must-follow rules.
```

## Initial chat messages

- **Messages inserted at the start of new threads for this character.**
- **Uses [AI]:, [USER]:, [SYSTEM; hiddenFrom=ai] syntax.**
- **These are summarized over time, unlike role/reminder.**

```md
[AI]: Hello.
[USER]: Hi.

[SYSTEM; hiddenFrom=ai]: This message is hidden from the AI.
```

## General writing instructions preset

- **Global writing style preset for the whole thread.**
- **Choose @roleplay1, @roleplay2, or @custom.**

```plaintext
@roleplay1
```

## General writing instructions (custom)

- **Only used when preset is @custom.**
- **Applies to the entire chat, not just this character.**

```md
- Each message includes dialogue and actions.
- Keep responses concise.
```

## Strict message length limit

- **Maximum paragraphs allowed per AI message.**
- **Empty means no limit.**

```plaintext
2
```

## User's name

- **Overrides the user's default name for this character.**

```plaintext
Alex
```

## User's description/role

- **Overrides the user's default description for this character.**

```md
{{user}} is a curious explorer who asks direct questions.
```

## User's avatar pic URL

- **Overrides the user's default avatar for this character.**

```url
https://user.uploads.dev/file/example-user-avatar.jpeg
```

## User reminder note

- **Reminder used when the AI writes on behalf of the user.**

```md
Keep user responses short and decisive.
```

## Default message style (color, font, size, etc.)

- **CSS-like style applied to this character's message bubble.**

```plaintext
color:#1f2a44; font-size:95%; background:rgba(240,244,255,0.6);
```

## Chat background image/video URL

- **Background image or video URL for the chat.**

```url
https://user.uploads.dev/file/example-background.webp
```

## Chat background music/audio URL

- **Background audio URL for the chat (mp3/ogg/webm/mp4).**

```url
https://user.uploads.dev/file/example-audio.mp3
```

## Image generation prompt starter

- **Prepended to every image prompt the AI generates.**
- **Supports Perchance and text-to-image prompt syntax.**

```plaintext
cinematic lighting, ultra-detailed,
```

## Image generation prompt ending

- **Appended to every image prompt the AI generates.**

```plaintext
, sharp focus, (negativePrompt:::blurry, low quality)
```

## Image prompt keyword triggers

- **Trigger format: trigger: description**
- **Use @prepend to add to the start.**
- **Regex triggers use /pattern/.**

```plaintext
Hero: A brave figure with a cape and steel gauntlets.
City: A neon-lit skyline with rain reflections.
/forest.?path/: A misty forest with dappled light.
Portrait: @prepend close-up portrait, neutral background,
```

## Lorebook URLs - one URL per line

- **Each URL points to a .txt file with blank-line-separated entries.**
- **Use /lore reload to update existing threads.**

```plaintext
https://user.uploads.dev/file/my-character-lore.txt
https://user.uploads.dev/file/my-world-lore.txt
```

## Method for fitting messages within model's context limit

- **summarizeOld or dropOld.**

```plaintext
summarizeOld
```

## Extended character memory

- **none or v1.**

```plaintext
v1
```

## Character avatar pic size

- **Multiplier for character avatar size (1.0 = default).**

```plaintext
1.0
```

## Character avatar shape

- **square, circle, or portrait.**

```plaintext
square
```

## User avatar pic size

- **Multiplier for user avatar size (blank uses default).**

```plaintext

```

## User avatar shape

- **default, square, circle, or portrait.**

```plaintext
default
```

## Shortcut buttons (above reply box)

- **Blocks with @name, @message, @insertionType, @autoSend.**
- **Applied to new threads only.**

```plaintext
@name=🗣️ {{char}}
@message=/ai <optional writing instruction>
@insertionType=replace
@autoSend=no

@name=🗣️ {{user}}
@message=/user <optional writing instruction>
@insertionType=replace
@autoSend=no

@name=🗣️ Narrator
@message=/nar <optional writing instruction>
@insertionType=replace
@autoSend=no

@name=🖼️ Image
@message=/image --num=3
@insertionType=replace
@autoSend=yes
```

## Custom JavaScript code

- **Runs in the Perchance runtime with access to oc.\* APIs.**

```javascript
oc.thread.on("MessageAdded", function ({ message }) {
  // Example: trim AI messages
  if (message.author === "ai") {
    message.content = message.content.trim();
  }
});
```

## System's name

- **Display name for system messages (if used).**

```plaintext
Narrator
```

## System's avatar pic URL

- **Avatar image used for system messages.**

```url
https://user.uploads.dev/file/example-system-avatar.webp
```

## Message input placeholder

- **Placeholder text shown in the reply box for this character.**

```plaintext
Type your reply to {{char}} here...
```

## Social media share link preview title

- **Custom title for share links.**

```plaintext
My Character - AI Chat
```

## Social media share link preview description

- **Custom description for share links.**

```plaintext
Chat with My Character, a friendly AI who helps you explore ideas.
```

## Social media share link preview image URL

- **Custom image for share link previews.**

```url
https://user.uploads.dev/file/example-share-image.webp
```
