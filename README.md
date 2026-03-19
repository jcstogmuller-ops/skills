> **Note:** This repository contains Anthropic's implementation of skills for Claude. For information about the Agent Skills standard, see [agentskills.io](http://agentskills.io).

# Skills
Skills are folders of instructions, scripts, and resources that Claude loads dynamically to improve performance on specialized tasks. Skills teach Claude how to complete specific tasks in a repeatable way, whether that's creating documents with your company's brand guidelines, analyzing data using your organization's specific workflows, or automating personal tasks.

For more information, check out:
- [What are skills?](https://support.claude.com/en/articles/12512176-what-are-skills)
- [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude)
- [How to create custom skills](https://support.claude.com/en/articles/12512198-creating-custom-skills)
- [Equipping agents for the real world with Agent Skills](https://anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills)

# About This Repository

This repository contains skills that demonstrate what's possible with Claude's skills system. These skills range from creative applications (art, music, design) to technical tasks (testing web apps, MCP server generation) to enterprise workflows (communications, branding, etc.).

Each skill is self-contained in its own folder with a `SKILL.md` file containing the instructions and metadata that Claude uses. Browse through these skills to get inspiration for your own skills or to understand different patterns and approaches.

Many skills in this repo are open source (Apache 2.0). We've also included the document creation & editing skills that power [Claude's document capabilities](https://www.anthropic.com/news/create-files) under the hood in the [`skills/docx`](./skills/docx), [`skills/pdf`](./skills/pdf), [`skills/pptx`](./skills/pptx), and [`skills/xlsx`](./skills/xlsx) subfolders. These are source-available, not open source, but we wanted to share these with developers as a reference for more complex skills that are actively used in a production AI application.

## Disclaimer

**These skills are provided for demonstration and educational purposes only.** While some of these capabilities may be available in Claude, the implementations and behaviors you receive from Claude may differ from what is shown in these skills. These skills are meant to illustrate patterns and possibilities. Always test skills thoroughly in your own environment before relying on them for critical tasks.

# Skill Sets
- [./skills](./skills): Skill examples for Creative & Design, Development & Technical, Enterprise & Communication, and Document Skills
- [./spec](./spec): The Agent Skills specification
- [./template](./template): Skill template

## Skills

### Creative & Design

| Skill | Description |
|-------|-------------|
| [algorithmic-art](./skills/algorithmic-art) | Creating algorithmic art using p5.js with seeded randomness and interactive parameter exploration. Use for generative art, flow fields, or particle systems. |
| [canvas-design](./skills/canvas-design) | Create beautiful visual art in .png and .pdf documents using design philosophy. Use when the user asks to create a poster, piece of art, design, or other static piece. |
| [frontend-design](./skills/frontend-design) | Create distinctive, production-grade frontend interfaces with high design quality. Use when building web components, pages, or applications with polished UI. |
| [slack-gif-creator](./skills/slack-gif-creator) | Knowledge and utilities for creating animated GIFs optimized for Slack. Use when users request animated GIFs for Slack. |
| [theme-factory](./skills/theme-factory) | Toolkit for styling artifacts with a theme (slides, docs, HTML landing pages, etc.). Includes 10 pre-set themes and on-the-fly theme generation. |
| [web-artifacts-builder](./skills/web-artifacts-builder) | Suite of tools for creating elaborate, multi-component HTML artifacts using React, Tailwind CSS, and shadcn/ui. Use for complex artifacts requiring state management or routing. |

### Development & Technical

| Skill | Description |
|-------|-------------|
| [claude-api](./skills/claude-api) | Build apps with the Claude API or Anthropic SDK. Triggers when code imports `anthropic`/`@anthropic-ai/sdk`/`claude_agent_sdk` or when asked to use Claude API or Agent SDK. |
| [mcp-builder](./skills/mcp-builder) | Guide for creating high-quality MCP (Model Context Protocol) servers in Python (FastMCP) or Node/TypeScript (MCP SDK) to integrate external APIs or services. |
| [skill-creator](./skills/skill-creator) | Create new skills, modify and improve existing skills, and measure skill performance. Use to create, edit, run evals, or optimize skill descriptions. |
| [webapp-testing](./skills/webapp-testing) | Toolkit for interacting with and testing local web applications using Playwright. Supports verifying frontend functionality, capturing screenshots, and viewing browser logs. |

### Enterprise & Communication

| Skill | Description |
|-------|-------------|
| [brand-guidelines](./skills/brand-guidelines) | Applies Anthropic's official brand colors and typography to artifacts. Use when brand colors, style guidelines, visual formatting, or company design standards apply. |
| [doc-coauthoring](./skills/doc-coauthoring) | Structured workflow for co-authoring documentation, proposals, technical specs, and decision docs through iterative refinement. |
| [internal-comms](./skills/internal-comms) | Helps write internal communications (status reports, leadership updates, newsletters, FAQs, incident reports, project updates) using company-preferred formats. |

### Document Skills

| Skill | Description |
|-------|-------------|
| [docx](./skills/docx) | Create, read, edit, or manipulate Word documents (.docx files), including formatting, tables of contents, headings, page numbers, and letterheads. |
| [pdf](./skills/pdf) | Work with PDF files: read/extract text and tables, combine/split PDFs, rotate pages, add watermarks, fill forms, encrypt/decrypt, extract images, and OCR. |
| [pptx](./skills/pptx) | Create, read, edit, or manipulate PowerPoint presentations (.pptx files), including slide decks, pitch decks, templates, layouts, and speaker notes. |
| [xlsx](./skills/xlsx) | Work with spreadsheet files (.xlsx, .xlsm, .csv, .tsv): open, read, edit, create, or convert between tabular formats, including formulas, charts, and data cleaning. |

# Try in Claude Code, Claude.ai, and the API

## Claude Code
You can register this repository as a Claude Code Plugin marketplace by running the following command in Claude Code:
```
/plugin marketplace add anthropics/skills
```

Then, to install a specific set of skills:
1. Select `Browse and install plugins`
2. Select `anthropic-agent-skills`
3. Select `document-skills` or `example-skills`
4. Select `Install now`

Alternatively, directly install either Plugin via:
```
/plugin install document-skills@anthropic-agent-skills
/plugin install example-skills@anthropic-agent-skills
```

After installing the plugin, you can use the skill by just mentioning it. For instance, if you install the `document-skills` plugin from the marketplace, you can ask Claude Code to do something like: "Use the PDF skill to extract the form fields from `path/to/some-file.pdf`"

## Claude.ai

These example skills are all already available to paid plans in Claude.ai. 

To use any skill from this repository or upload custom skills, follow the instructions in [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude#h_a4222fa77b).

## Claude API

You can use Anthropic's pre-built skills, and upload custom skills, via the Claude API. See the [Skills API Quickstart](https://docs.claude.com/en/api/skills-guide#creating-a-skill) for more.

# Creating a Basic Skill

Skills are simple to create - just a folder with a `SKILL.md` file containing YAML frontmatter and instructions. You can use the **template-skill** in this repository as a starting point:

```markdown
---
name: my-skill-name
description: A clear description of what this skill does and when to use it
---

# My Skill Name

[Add your instructions here that Claude will follow when this skill is active]

## Examples
- Example usage 1
- Example usage 2

## Guidelines
- Guideline 1
- Guideline 2
```

The frontmatter requires only two fields:
- `name` - A unique identifier for your skill (lowercase, hyphens for spaces)
- `description` - A complete description of what the skill does and when to use it

The markdown content below contains the instructions, examples, and guidelines that Claude will follow. For more details, see [How to create custom skills](https://support.claude.com/en/articles/12512198-creating-custom-skills).

# Partner Skills

Skills are a great way to teach Claude how to get better at using specific pieces of software. As we see awesome example skills from partners, we may highlight some of them here:

- **Notion** - [Notion Skills for Claude](https://www.notion.so/notiondevs/Notion-Skills-for-Claude-28da4445d27180c7af1df7d8615723d0)
