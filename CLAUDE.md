# Markdown Formatting Guidelines

This document contains style guidelines for writing Markdown in this project.

## General Rules

- No more than one sentence per line
- Always put a blank line before lists
- Don't use bold formatting as a substitute for proper headings
- Use headings (##, ###, ####) for hierarchical organization

## Headings

Use proper heading hierarchy and sentence case capitalization:

```markdown
## Main section
### Subsection
#### Sub-subsection
```

**Capitalization rule**: Use sentence case - capitalize only the first word and proper nouns:

```markdown
<!-- Good -->
## Climate risk assessment
### What is extreme value theory?
#### Bayesian inference methods

<!-- Bad -->
## Climate Risk Assessment
### What Is Extreme Value Theory?
#### Bayesian Inference Methods
```

Don't use bold text instead of headings:

```markdown
<!-- Bad -->
**Learning Resources:**

<!-- Good -->
### Learning resources
```

## Lists

Always include a blank line before lists:

```markdown
<!-- Bad -->
Here are the options:
- Option 1
- Option 2

<!-- Good -->
Here are the options:

- Option 1
- Option 2
```

## Introducing Lists

Instead of using bold text to introduce lists, use natural language:

```markdown
<!-- Bad -->
**Learning Resources:**
- Resource 1
- Resource 2

<!-- Good -->
You can learn more at:

- Resource 1
- Resource 2
```

## Line Length

Keep to one sentence per line for better readability and version control:

```markdown
<!-- Bad -->
This is a very long sentence that contains multiple ideas and should be broken up into separate lines for better readability and version control tracking.

<!-- Good -->
This is a sentence that expresses one idea.
This is another sentence that expresses a different idea.
```

## Bold and Emphasis

Use bold sparingly and only for true emphasis, not for pseudo-headings:

```markdown
<!-- Use bold for emphasis -->
This is *really* important.

<!-- Don't use bold for headings -->
**Section Title** <!-- Use ### Section Title instead -->
```