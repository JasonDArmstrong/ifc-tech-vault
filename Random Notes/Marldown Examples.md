---
tags: [reference]
---
# Comprehensive Markdown Guide for Obsidian

## Table of Contents
1. [Headings](#headings)
2. [Text Formatting](#text-formatting)
3. [Lists](#lists)
4. [Links](#links)
5. [Images](#images)
6. [Blockquotes](#blockquotes)
7. [Code](#code)
8. [Tables](#tables)
9. [Footnotes](#footnotes)
10. [Horizontal Rules](#horizontal-rules)
11. [Task Lists](#task-lists)
12. [Math](#math)
13. [Embeds](#embeds)
14. [Comments](#comments)
15. [Admonitions](#admonitions)

---

## Headings
Use `#` followed by a space for the heading levels. More `#` symbols indicate a smaller heading size.

```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

## Text Formatting
You can emphasize text by making it bold or italic, or both.

```markdown
*Italic* or _Italic_
**Bold**
***Bold and Italic*** or ___Bold and Italic___
~~Strikethrough~~
```

## Lists
### Unordered Lists
Use `-`, `+`, or `*` followed by a space.

```markdown
- Item 1
- Item 2
  - Subitem 2.1
  - Subitem 2.2

+ Item 1
+ Item 2
  + Subitem 2.1
  + Subitem 2.2

* Item 1
* Item 2
  * Subitem 2.1
  * Subitem 2.2


### Ordered Lists
Use numbers followed by a period.

```markdown
1. First item
2. Second item
   1. Subitem 2.1
   2. Subitem 2.2
```

## Links
### Standard Links
```markdown
[Obsidian](https://obsidian.md)
```

### Reference Links
```markdown
[Obsidian][1]

[1]: https://obsidian.md
```

## Images
### Standard Images
```markdown
![Alt text](https://obsidian.md/images/logo.png)
```

### Reference Images
```markdown
![Alt text][logo]

[logo]: https://obsidian.md/images/logo.png
```

## Blockquotes
Use `>` followed by a space.

```markdown
> This is a blockquote.
> 
> Another line in the same blockquote.
```

## Code
### Inline Code
Use backticks `` ` ``.

```markdown
Here is some `inline code`.
```

### Code Blocks
Use triple backticks ``` ``` or indent with four spaces.

    ```python
    def hello_world():
        print("Hello, world!")
    ```

    or

        def hello_world():
            print("Hello, world!")
```

## Tables
```markdown
| Header 1 | Header 2 |
|----------|----------|
| Row 1    | Data 1   |
| Row 2    | Data 2   |
```

## Footnotes
```markdown
Here is a footnote reference[^1].

[^1]: This is the footnote content.
```

## Horizontal Rules
Use three or more `-`, `*`, or `_`.

```markdown
---
***
___
```

## Task Lists
Use `- [ ]` for an incomplete task and `- [x]` for a completed task.

```markdown
- [ ] Task 1
- [x] Task 2
```

## Math
### Inline Math
Use single dollar signs `$`.

```markdown
Inline math: $E = mc^2$
```

### Block Math
Use double dollar signs `$$`.

```markdown
$$
E = mc^2
$$
```

## Embeds
### Embed Internal Note
```markdown
![[Internal Note]]
```

### Embed PDF
```markdown
![[example.pdf]]
```

## Comments
Use `%%` to comment out text.

```markdown
%% This is a comment and won't be rendered %%
```

## Admonitions
### Info Admonition
```markdown
```ad-info
Title
Content of the info admonition.
```
```

### Warning Admonition
```markdown
```ad-warning
Title
Content of the warning admonition.
```
```

### Note Admonition
```markdown
```ad-note
Title
Content of the note admonition.
```
```

This guide covers the essential Markdown syntax you can use in Obsidian to structure and style your notes. Obsidian also supports several plugins and features that extend the basic Markdown functionality, so be sure to explore those to enhance your note-taking experience.