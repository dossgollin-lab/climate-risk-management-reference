# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.
This "AI" tool is used for syntax polishing and proofreading, occasionally for reorganizing text and code, but **never for research or content.**

## Project Overview

This is a Quarto book project for "Hydroclimate Risk Assessment and Management" - a comprehensive textbook on climate risk management using Julia for computational examples. The book is structured in three parts:

1. **Part I: Building Blocks** - Fundamentals of probability, statistics, optimization, and machine learning
2. **Part II: Hydroclimate Extremes and Catastrophes** - Hazard assessment and modeling climate extremes  
3. **Part III: Risk Analysis and Management** - Risk mapping and management interventions

## Key Technologies

- **Quarto**: Document publishing system that combines markdown with executable code
- **Julia**: Programming language used for all computational notebooks and examples

## Essential Commands

- `quarto preview` - Start live preview server (default port 4200)
- `quarto render` - Build the entire book to HTML
- `quarto publish` - Publish book (when configured)
- `quarto clean` - Clean build artifacts

## Project Structure

### Core Configuration

- `_quarto.yml` - Main Quarto configuration defining book structure, chapters, and output formats
- `Project.toml` - Julia project file listing dependencies (CSV, DataFrames, Distributions, Extremes, etc.)
- `Manifest.toml` - Julia dependency lockfile
- `references.bib` - Bibliography file
- `_variables.yml` - Quarto variables

### Content Organization

- `index.qmd` - Book homepage and introduction
- `chapters/` - Main book chapters organized by part:
  - `fundamentals/` - Statistics, optimization, ML foundations
  - `hazard/` - Climate hazard modeling chapters
  - `risk/` - Risk management chapters
  - `appendices/` - Additional reference material
- `notebooks/` - Computational case studies and tutorials
- `pages/` - Standalone pages (author, contribute)

### Build Artifacts

- `_book/` - Generated HTML output
- `_freeze/` - Cached computation results for faster rebuilds

## Development Workflow

1. **Content Creation**: Write in `.qmd` files using Quarto markdown syntax
2. **Julia Code**: Include Julia code blocks that execute during rendering
3. **Preview**: Use `quarto preview` for live development
4. **Dependencies**: Manage Julia packages through `Project.toml`

## Julia Code Conventions

This book uses a single Julia project with a single environment.

- Use Makie for plots, NOT Plots.jl
- Use `CairoMakie.activate!(; type="svg")` for high-quality plots
- Import required packages at the beginning of notebooks
- Follow existing patterns in computational notebooks for consistency
- Leverage domain-specific packages like `Extremes.jl` for specialized analysis

### Notebooks

Each notebook is designed to be a standalone git repository with its own Julia repository for easily maintenance.
Each should be included as a submodule.

## Content Guidelines

- Each chapter includes learning objectives and references
- Computational notebooks demonstrate practical applications
- Content is modular - chapters can be read independently
- Mathematical notation follows standard conventions in the field
- All content is licensed under CC BY-SA 4.0

## Writing Style

- Use one sentence per line in markdown files for better version control and editing
- This applies to all `.qmd` files including chapters, index, and preface

## Chapter Status System

Each chapter and page uses a 4-level emoji-based status tracking system:

- 🚧 **Planning** - Initial brainstorming and outlining stage. Structure identified but content not yet written.
- 📝 **Draft** - Substantial content written but may have gaps, need reorganization, or require additional examples.
- ✏️ **Revision** - Complete draft exists but needs editing for clarity, accuracy, and consistency.
- 🎯 **Ready** - Content complete, polished, and has undergone final review. Ready for use.

### Implementation:
- Status emoji appears at the end of chapter titles: `# Chapter Title 📝`
- Each chapter includes a status callout near the top explaining the current status and the 4-part scale
- Status should be updated as chapters progress through development stages

## Execution Environment

- Julia 1.11+ required
- Quarto execution uses `jupyter: julia-1.11` kernel
- Computation caching enabled with `freeze: auto` and `cache: true`
- Notebook outputs frozen to avoid unnecessary recomputation
