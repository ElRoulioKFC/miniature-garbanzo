# Markdown Cheatsheet

```markdown
## Headings
Use `#` to `######` for headings.

```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

## Text Formatting

- **Bold**: `**bold**` or `__bold__`
- *Italic*: `*italic*` or `_italic_`
- ~~Strikethrough~~: `~~strikethrough~~`
- **Inline Code**: `` `inline code` ``

## Lists

### Unordered Lists

Use `*`, `+`, or `-` for unordered lists.

```markdown
* Item 1
* Item 2
  * Subitem 1
  * Subitem 2
```

### Ordered Lists

Use numbers followed by a period.

```markdown
1. Item 1
2. Item 2
   1. Subitem 1
   2. Subitem 2
```

## Links

### Inline Link

```markdown
[OpenAI](https://www.openai.com)
```

### Reference Link

```markdown
[OpenAI][1]

[1]: https://www.openai.com
```

## Images

### Inline Image

```markdown
![Alt text](https://example.com/image.jpg)
```

### Reference Image

```markdown
![Alt text][logo]

[logo]: https://example.com/image.jpg
```

## Code

### Inline Code

Use single backticks ` for inline code.

Here is `inline code`.

### Code Blocks

Use triple backticks for code blocks. Optionally, specify the language for syntax highlighting.

```python
def hello_world():
    print("Hello, World!")
```

### Syntax Highlighting

Specify the language for syntax highlighting (e.g., `python`, `javascript`).

```javascript
console.log("Hello, World!");
```

## Blockquotes

Use `>` for blockquotes. Nested blockquotes are supported.

> This is a blockquote.
> 
> This is a new paragraph within the blockquote.
> 
> > Nested blockquote

## Horizontal Rules

Use three or more dashes, asterisks, or underscores.

```markdown
---
***
___
```

## Tables

Create tables with pipes `|` and dashes `-`. Use colons for alignment.

| Header 1 | Header 2 | Header 3 |
|:---------|:---------|:---------|
| Left-aligned | Center-aligned | Right-aligned |
| Row 1    | Data     | More Data|
| Row 2    | Data     | More Data|



## Definition Lists

Use `Term` and `: Definition` for definition lists.

```markdown
Term 1
: Definition 1

Term 2
: Definition 2
```

## Custom HTML

You can use raw HTML for more control.

```html
<p>This is a paragraph in HTML.</p>
```

## Emojis

Use emojis by referencing their shortcodes.

```markdown
:smile: :thumbsup: :rocket:
```

## Links with Titles

Add titles to links for additional context.

```markdown
[OpenAI](https://www.openai.com "OpenAI Homepage")
```

## Mentions

Use `@` to mention users in some Markdown-based platforms.

```markdown
@username
```

## Advanced Features

### Footnote Formatting

Footnotes can be formatted with more complex Markdown or HTML if needed.

```markdown
[^1]: This is a detailed footnote with `inline code` and **bold text**.
```

### Custom Attributes

In some Markdown flavors, you can use custom attributes for advanced customization.

```html
<div class="custom-class">
  <p>This is a div with a custom class.</p>
</div>
```

### Collapsible Sections

Some Markdown platforms support collapsible sections.

<details>
<summary>Click to expand</summary>

This is the content that will be revealed when the section is expanded.

</details>

### Metadata and Front Matter

Many Markdown files use YAML front matter for metadata.

```markdown
---
title: "Document Title"
author: "Author Name"
date: "2024-07-23"
---

# Main Content
```

### Comment Syntax

Some implementations allow comments in Markdown.

```markdown
<!-- This is a comment and will not be visible in the rendered output. -->
```

### Linking to Specific Sections

You can link to specific sections within a document.

```markdown
[Go to Heading 2](#heading-2)
```

### Embedded Content

Embedding content such as iframes might be supported depending on the Markdown renderer.

```html
<iframe src="https://example.com" width="600" height="400"></iframe>
```

### Interactive Elements

For platforms like GitHub, task lists and other interactive elements can be used.

```markdown
- [ ] Task 1
- [x] Task 2
```

## Best Practices

1. **Consistent Formatting**: Keep your formatting consistent for readability.
2. **Use Headings Wisely**: Structure your document with clear and consistent headings.
3. **Preview Your Markdown**: Always preview your Markdown to check how it renders.
4. **Keep It Simple**: Avoid overly complex structures; simplicity enhances readability.
5. **Leverage Extended Syntax**: Utilize extended Markdown features if supported by your platform.

---

Feel free to adapt this cheatsheet to better suit your specific needs. Happy documenting!
```