# Writing Guidelines for Climate Risk Management Reference

This document contains style guidelines for writing content in this project, covering both formatting and pedagogical approach.

## Markdown Formatting

### General Rules

- No more than one sentence per line
- Always put a blank line before lists
- Don't use bold formatting as a substitute for proper headings
- Use headings (##, ###, ####) for hierarchical organization

### Headings

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

**Avoid "peppy" or overselling language** in headings and text:

```markdown
<!-- Bad -->
### Computing expectations: The goal of inference!
### Joint distributions as the central object

<!-- Good -->
### Computing expectations
### Joint distributions
```

Don't use bold text instead of headings:

```markdown
<!-- Bad -->
**Learning Resources:**

<!-- Good -->
### Learning resources
```

### Lists

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

### Line Length

Keep to one sentence per line for better readability and version control:

```markdown
<!-- Bad -->
This is a very long sentence that contains multiple ideas and should be broken up into separate lines for better readability and version control tracking.

<!-- Good -->
This is a sentence that expresses one idea.
This is another sentence that expresses a different idea.
```

### Bold and Emphasis

Use bold sparingly and only for true emphasis, not for pseudo-headings:

```markdown
<!-- Use bold for emphasis -->
This is *really* important.

<!-- Don't use bold for headings -->
**Section Title** <!-- Use ### Section Title instead -->
```

## Mathematical Notation

### Probability Notation

Use consistent notation throughout:

- **Densities and continuous distributions**: Use lowercase `p(x)`, `p(x, y)`, `p(θ | y)`
- **Discrete probabilities and events**: Use `Pr(X = x)`, `Pr(A ∩ B)`
- **Parameters**: `θ` (theta)
- **Observed data**: `y`
- **Predictions**: `ỹ` (y-tilde)

```markdown
<!-- Good -->
The posterior density p(θ | y) represents our updated beliefs.
The probability Pr(flood next year) = 0.1 represents a discrete event.

<!-- Inconsistent -->
The posterior P(θ | y) and probability p(flood) = 0.1
```

### LaTeX Math

- Always use proper LaTeX notation in dollar signs, never Unicode symbols
- Use `\mathbb{E}` for expectation, `\text{}` for text in math mode
- Use `\sim` for "distributed as": `Y \sim \text{Normal}(0, 1)`

```markdown
<!-- Good -->
$$\mathbb{E}[X] = \int_{-\infty}^{\infty} x p(x) dx$$

<!-- Bad -->
E[X] = ∫ x p(x) dx (Unicode symbols)
```

## Pedagogical Approach

### Chapter Structure

Follow this general structure for technical chapters:

1. **Opening workflow/motivation**: Start with the "why" and "what" before diving into details
2. **Simple concrete example**: Use pedagogically clean examples (like coin flipping) before domain-specific ones
3. **Essential operations**: Teach core concepts needed for the workflow  
4. **Building blocks**: Provide detailed mathematical tools
5. **Context and extensions**: Philosophical, computational, or advanced topics

### Writing Style

**Show, don't tell**: Let the mathematics and examples speak rather than using enthusiastic language.

```markdown
<!-- Bad -->
Expectation is everything for risk assessment!
This is the most important concept in probability theory!

<!-- Good -->
Most decision-relevant quantities can be expressed as expectations.
Expectations provide the bridge between probability models and decisions.
```

**Use restrained, academic tone**: Avoid overselling concepts or using marketing-style language.

### Examples and Motivation

**Start simple, then build complexity**:

```markdown
<!-- Good progression -->
1. Coin flipping example (simple, pedagogically clean)
2. Brief connection to climate risk to show relevance  
3. More complex applications after fundamentals are established

<!-- Bad progression -->
1. Complex ENSO/flood example with domain-specific concepts
2. Students get lost in details before learning fundamentals
```

**Connect simple examples to the domain**: Add brief sentences showing how simple examples relate to climate risk without making them complex.

### Avoiding Common Pitfalls

**Don't introduce confusing concepts**: Some concepts that seem important can be pedagogically confusing:

```markdown
<!-- Confusing - avoid separate "transformation" discussion -->
Three operations: conditioning, marginalization, transformation
(Students get confused about when to use what)

<!-- Clearer -->  
Two operations: conditioning and marginalization
Both serve one purpose: computing expectations
(Transformations happen naturally within expectation calculations)
```

**Don't interrupt the main narrative flow**: Move detailed but tangential material to later sections:

```markdown
<!-- Bad flow -->
1. Core inference workflow
2. Long list of probability distributions (interrupts flow)
3. Back to inference operations

<!-- Good flow -->
1. Core inference workflow  
2. Essential inference operations
3. Building blocks section (distributions, etc.)
```

**Maintain consistent level of mathematical rigor**: Don't alternate between overly simple and overly complex explanations.

## Content Organization

### Section Ordering

For probability/statistics chapters, this ordering works well:

1. **Workflow introduction** (three steps + simple example)
2. **Essential operations** (the core tools students need)
3. **Interpretation** (what do these concepts mean?)
4. **Computational approaches** (how to actually calculate things)
5. **Building blocks** (detailed mathematical tools)
6. **Advanced topics** (extensions, special cases)

### Examples and Applications

- Use **simple examples first** for pedagogical clarity
- Add **brief connections** to show relevance to climate risk
- Save **complex applications** for after fundamentals are solid
- Provide **concrete climate examples** in later sections/chapters

This approach balances pedagogical clarity with domain relevance, following the successful pattern from BDA3 and other effective technical textbooks.