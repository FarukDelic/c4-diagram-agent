# AI Digital Modernization

This repository contains tools for analyzing and modernizing legacy codebases using AI-powered architecture analysis and documentation generation.

## Setup Instructions

### 1. Install PromptRepository

```bash
cd PromptRepository
npm install
npm run build
```

### 2. Install C4Diagrammer

```bash
cd C4Diagrammer
npm install
npm run build
```

### 3. Start Claude

Open your terminal and run:

```bash
claude
```

### 4. Clone Your Project

Navigate to the `codebase` folder and clone your project:

```bash
cd codebase
git clone <your-project-url>
```

### 5. Configure Claude Agent

Before starting analysis, you need to update the agent configuration to match your file system:

1. Open `.claude/agents/c4-architecture-analyzer.md`
2. Update line 9 to point to your C4Diagrammer installation:
   ```
   args: ["/path/to/your/ai-digital-modernization/C4Diagrammer/dist/src/index.js", "/path/to/your/ai-digital-modernization/codebase"]
   ```
   Replace `/path/to/your/` with your actual file system path.

### 6. Start Analysis

In Claude, use the following prompt to begin analyzing your codebase:

```
use subagent to analyze the codebase @codebase folder
```

## Project Structure

- **PromptRepository/**: Contains prompt management and chat functionality for AI interactions
- **C4Diagrammer/**: Generates C4 architecture diagrams from code analysis
- **codebase/**: Directory for storing projects to be analyzed (includes example `livvy-assist-rag-poc`)

## Features

- **Automated Architecture Analysis**: Analyze legacy codebases and generate comprehensive architecture documentation
- **C4 Diagram Generation**: Create visual architecture diagrams following C4 model conventions
- **AI-Powered Documentation**: Generate high-level documentation from existing code structures
- **Legacy Code Modernization**: Identify modernization opportunities and architectural improvements
