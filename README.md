# PAM BMad-Method: Universal AI Agent Framework

[![Version](https://img.shields.io/badge/version-1.0.0-blue)](1.0.0)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Node.js Version](https://img.shields.io/badge/node-%3E%3D20.0.0-brightgreen)](https://nodejs.org)

Foundations in Agentic Agile Driven Development, known as the Breakthrough Method of Agile AI-Driven Development, yet so much more. Transform any domain with specialized AI expertise: software development, entertainment, creative writing, business strategy to personal wellness just to name a few.

This is a fork of the original [BMad-Method repository](https://github.com/bmadcode/BMAD-METHOD). All credits to the original author.

It has been modified to for personal use.

## Overview

**BMad Method's Two Key Innovations:**

**1. Agentic Planning:** Dedicated agents (Analyst, PM, Architect) collaborate with you to create detailed, consistent PRDs and Architecture documents. Through advanced prompt engineering and human-in-the-loop refinement, these planning agents produce comprehensive specifications that go far beyond generic AI task generation.

**2. Context-Engineered Development:** The Scrum Master agent then transforms these detailed plans into hyper-detailed development stories that contain everything the Dev agent needs - full context, implementation details, and architectural guidance embedded directly in story files.

This two-phase approach eliminates both **planning inconsistency** and **context loss** - the biggest problems in AI-assisted development. Your Dev agent opens a story file with complete understanding of what to build, how to build it, and why.

**📖 [See the complete workflow in the User Guide](bmad-core/user-guide.md)** - Planning phase, development cycle, and all agent roles

## Quick Navigation

### Understanding the BMad Workflow

**Before diving in, review these critical workflow diagrams that explain how BMad works:**

1. **[Planning Workflow (Web UI)](bmad-core/user-guide.md#the-planning-workflow-web-ui)** - How to create PRD and Architecture documents
2. **[Core Development Cycle (IDE)](bmad-core/user-guide.md#the-core-development-cycle-ide)** - How SM, Dev, and QA agents collaborate through story files

> ⚠️ **These diagrams explain 90% of BMad Method Agentic Agile flow confusion** - Understanding the PRD+Architecture creation and the SM/Dev/QA workflow and how agents pass notes through story files is essential - and also explains why this is NOT taskmaster or just a simple task runner!

### What would you like to do?

- **[Install and Build software with Full Stack Agile AI Team](#quick-start)** → Quick Start Instruction
- **[Learn how to use BMad](bmad-core/user-guide.md)** → Complete user guide and walkthrough
- **[See available AI agents](/bmad-core/agents))** → Specialized roles for your team
- **[Explore non-technical uses](#-beyond-software-development---expansion-packs)** → Creative writing, business, wellness, education
- **[Create my own AI agents](docs/creating-expansion-pack.md)** → Build agents for your domain
- **[Browse ready-made expansion packs](expansion-packs/)** → DevOps, infrastructure and get inspired with ideas and examples
- **[Understand the architecture](docs/core-architecture.md)** → Technical deep dive

## Quick Start & Updates

### One Command for Everything

Whether you're installing for the first time, upgrading an existing installation, or adding expansion packs, just run this single command in your project's directory:

```bash
npx pam-bmad install
```

This command handles everything automatically:
- ✅ **New Installations:** Sets up BMad in your project.
- ✅ **Upgrades:** Updates existing installations, preserving your custom configurations by creating `.bak` files for any modified files.
- ✅ **Expansion Packs:** Installs any expansion packs you've added to `package.json`.

**Prerequisites**: [Node.js](https://nodejs.org) v20+ required.

### For BMad Developers (Contributing)

If you have cloned the `pam-bmad` repository to contribute to its development, use the following commands to update your local clone and run the installer:

```bash
git pull
npm run install:pam-bmad
```

### Fastest Start: Web UI Full Stack Team at your disposal (2 minutes)

1. **Get the bundle**: Save or clone the [full stack team file](dist/teams/team-fullstack.txt) or choose another team
2. **Create AI agent**: Start a new Chat with your IDEs AI Agent.
3. **Upload & configure**: Upload the file and set instructions: "Your critical operating instructions are attached, do not break character as directed"
4. **Start Ideating and Planning**: Start chatting! Type `*help` to see available commands or pick an agent like `*analyst` to start right in on creating a brief.
5. **CRITICAL**: Talk to BMad Orchestrator in the web at ANY TIME (#bmad-orchestrator command) and ask it questions about how this all works!
6. **When to move to the IDE**: Once you have your PRD, Architecture, optional UX and Briefs - its time to switch over to the IDE to shard your docs, and start implementing the actual code! See the [User guide](bmad-core/user-guide.md) for more details



## 🌟 Beyond Software Development - Expansion Packs

BMad's natural language framework works in ANY domain. Expansion packs provide specialized AI agents for creative writing, business strategy, health & wellness, education, and more. Also expansion packs can expand the core BMad-Method with specific functionality that is not generic for all cases. [See the Expansion Packs Guide](docs/expansion-packs.md) and learn to create your own!

## Codebase Flattener Tool

The BMad-Method includes a powerful codebase flattener tool designed to prepare your project files for AI model consumption. This tool aggregates your entire codebase into a single XML file, making it easy to share your project context with AI assistants for analysis, debugging, or development assistance.

### Features

- **AI-Optimized Output**: Generates clean XML format specifically designed for AI model consumption
- **Smart Filtering**: Automatically respects `.gitignore` patterns to exclude unnecessary files
- **Binary File Detection**: Intelligently identifies and excludes binary files, focusing on source code
- **Progress Tracking**: Real-time progress indicators and comprehensive completion statistics
- **Flexible Output**: Customizable output file location and naming

### Usage

```bash
# Basic usage - creates flattened-codebase.xml in current directory
npx pam-bmad flatten

# Minimal output - only file paths and metadata, no code content
npx pam-bmad flatten --minimal

# Specify custom input directory
npx pam-bmad flatten --input /path/to/source/directory
npx pam-bmad flatten -i /path/to/source/directory

# Specify custom output file
npx pam-bmad flatten --output my-project.xml
npx pam-bmad flatten -o /path/to/output/codebase.xml

# Combine input and output options
npx pam-bmad flatten --input /path/to/source --output /path/to/output/codebase.xml
```

### Example Output

The tool will display progress and provide a comprehensive summary:

```
📊 Completion Summary:
✅ Successfully processed 156 files into flattened-codebase.xml
📁 Output file: /path/to/your/project/flattened-codebase.xml
📏 Total source size: 2.3 MB
📄 Generated XML size: 2.1 MB
📝 Total lines of code: 15,847
🔢 Estimated tokens: 542,891
📊 File breakdown: 142 text, 14 binary, 0 errors
```

The generated XML file contains all your project's source code in a structured format that AI models can easily parse and understand, making it perfect for code reviews, architecture discussions, or getting AI assistance with your BMad-Method projects.

## Documentation & Resources

### Essential Guides

- 📖 **[User Guide](bmad-core/user-guide.md)** - Complete walkthrough from project inception to completion
- 🏗️ **[Core Architecture](docs/core-architecture.md)** - Technical deep dive and system design
- 🚀 **[Expansion Packs Guide](docs/expansion-packs.md)** - Extend BMad to any domain beyond software development

## PAM BMad-Method Support

- 🐛 [Issue Tracker](https://github.com/pietermyb/pam-bmad/issues)
- 💬 [Discussions](https://github.com/pietermyb/pam-bmad/discussions)

## Original BMAD Method Support

- 💬 [Discord Community](https://discord.gg/gk8jAdXWmj)
- 🐛 [Issue Tracker](https://github.com/bmadcode/bmad/issues)
- 💬 [Discussions](https://github.com/bmadcode/bmad/discussions)

## Contributing

**We're excited about contributions and welcome your ideas, improvements, and expansion packs!** 🎉

📋 **[Read CONTRIBUTING.md](CONTRIBUTING.md)** - Complete guide to contributing, including guidelines, process, and requirements

## License

MIT License - see [LICENSE](LICENSE) for details.

<sub>Built with ❤️ for the AI-assisted development community</sub>
