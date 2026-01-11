# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a Claude Skills Library - a curated collection of reusable skills/workflows for Claude Code. The repository contains:

1. **Skills** organized into four categories (development, devops, documentation, automation)
2. **Claude Code Skill Creator** (`claude-code-skill-creator/`) - a toolkit for creating new skills with templates and validation
3. **Documentation** guiding contributors on writing and organizing skills

## Repository Structure

```
claude-skills/
├── skills/                          # Organized skills by category
│   ├── development/                 # Code writing, testing, debugging
│   ├── devops/                      # Infrastructure, deployment, CI/CD
│   ├── documentation/               # Doc generation, formatting
│   └── automation/                  # Task automation, workflows
│
├── claude-code-skill-creator/       # Skill creation toolkit (subproject)
│   ├── scripts/                     # Bash scripts for skill creation/validation
│   │   ├── create-skill.sh          # Interactive wizard to create skills
│   │   ├── validate-skill.sh        # Validates skill structure/content
│   │   ├── copy-template.sh         # Quick template copying
│   │   └── lib/                     # Shared utilities (colors, prompts, validators)
│   └── templates/                   # Skill templates (basic, with-scripts, with-config)
│
├── docs/                            # Project documentation
│   ├── SKILL_GUIDELINES.md          # How to write good skills
│   └── CATEGORIES.md                # Category definitions and selection guide
│
├── SKILL_TEMPLATE.md                # Template for creating new skills
├── CONTRIBUTING.md                  # Contribution guidelines
└── README.md                        # Main documentation
```

## Key Concepts

### Skill Structure

Each skill is self-contained in its own directory and must include:
- **SKILL.md** - Main documentation (required sections: skill name, overview, instructions, examples, Apache 2.0 license footer)
- **LICENSE** - Apache 2.0 license file
- **Optional**: `scripts/`, `config/`, `assets/` directories for helper files

### Skill Categories

Skills are organized by primary purpose:
- **development/** - Writing/testing/debugging code
- **devops/** - Infrastructure/deployment/operations
- **documentation/** - Creating/managing documentation
- **automation/** - Automating repetitive tasks

## Common Commands

### Creating a New Skill

Using the interactive wizard (recommended):
```bash
cd claude-code-skill-creator
./scripts/create-skill.sh
```

Quick template copy:
```bash
cd claude-code-skill-creator
./scripts/copy-template.sh basic my-skill-name ../skills/category-name
```

Manual creation:
```bash
mkdir -p skills/category-name/skill-name
cp SKILL_TEMPLATE.md skills/category-name/skill-name/SKILL.md
# Edit the SKILL.md file to fill in all {{PLACEHOLDERS}}
```

### Validating a Skill

Validate skill structure and content:
```bash
./claude-code-skill-creator/scripts/validate-skill.sh skills/category/skill-name
```

This checks for:
- Required files (SKILL.md, LICENSE)
- Apache 2.0 license
- Skill name and required sections
- Template placeholders ({{...}})
- TODO/FIXME markers
- Balanced markdown code blocks

### Searching for Skills

Find skills by pattern:
```bash
find skills -name "SKILL.md" | xargs grep -l "keyword"
```

Search within skill content:
```bash
grep -r "keyword" skills/*/SKILL.md
```

List all skills by category:
```bash
ls skills/development/
ls skills/devops/
ls skills/documentation/
ls skills/automation/
```

## Development Workflow

### Adding a New Skill

1. Determine the correct category (see `docs/CATEGORIES.md`)
2. Create the skill using the wizard or manually
3. Fill in all required sections in SKILL.md:
   - Skill name (H1 header)
   - Overview (2-4 sentences)
   - When to Use This Skill
   - Prerequisites (with versions)
   - Step-by-step instructions
   - At least one complete working example
   - Apache 2.0 license footer
4. Remove all template placeholders ({{...}})
5. Validate with `validate-skill.sh`
6. Test all examples thoroughly
7. Submit PR with commit message: `feat(category): add skill-name`

### Updating an Existing Skill

1. Create branch: `git checkout -b update/skill-name`
2. Make changes to the skill
3. Test all examples still work
4. Validate with `validate-skill.sh`
5. Submit PR describing changes

## Skill Writing Guidelines

### Required Content
- Clear, descriptive skill name (under 50 chars)
- Overview explaining what it does and why it's useful
- Specific use cases (3-5 bullet points)
- Complete prerequisites with version requirements
- Step-by-step instructions with code examples
- At least one complete, tested example with expected output
- Apache 2.0 license footer

### Content Standards
- Use active voice and present tense
- Use second person ("you")
- Always specify language in code blocks (\`\`\`bash, \`\`\`python, etc.)
- Show expected output for examples
- Include troubleshooting for common issues
- No sensitive data (API keys, passwords, etc.)
- No incomplete placeholders in final version

### Validation Checklist
- All template {{PLACEHOLDERS}} replaced
- No TODO/FIXME markers
- Code blocks are balanced (even number of \`\`\`)
- Examples are tested and working
- License footer included
- Prerequisites clearly listed with versions
- Current copyright year

## Architecture Notes

### Script Organization (claude-code-skill-creator/)

The skill creator toolkit uses a modular script architecture:

- **Main scripts** (`create-skill.sh`, `validate-skill.sh`, `copy-template.sh`) - User-facing entry points
- **Library modules** (`scripts/lib/`) - Shared utilities:
  - `colors.sh` - Terminal color codes and formatting
  - `prompts.sh` - Interactive prompts and user input
  - `validators.sh` - Validation functions for skill content
- **Templates** - Three template types:
  - `basic` - Simple SKILL.md only
  - `with-scripts` - Includes scripts/ directory
  - `with-config` - Includes config/ directory

### Template System

Templates use {{PLACEHOLDER}} syntax replaced by `sed` during creation. The wizard mode provides helpful defaults for all placeholders, while manual creation requires filling them in.

### Validation Strategy

The validator (`validate-skill.sh`) checks:
1. File existence (SKILL.md, LICENSE)
2. License type (must be Apache 2.0)
3. Required sections in SKILL.md
4. Placeholder remnants
5. Markdown syntax (balanced code blocks)
6. Content completeness (minimum 20 lines)
7. Copyright year currency

## Contributing Standards

### Prohibited Content
- Sensitive data (API keys, passwords, credentials)
- Proprietary or copyrighted code
- Malicious content
- Personal information
- Incomplete or untested skills

### Commit Message Format
Follow conventional commits:
- `feat(category): add skill-name` - New skill
- `fix(category): correct issue in skill-name` - Bug fix
- `docs: update SKILL_GUIDELINES` - Documentation
- `chore: update dependencies` - Maintenance

### PR Requirements
- Skill in correct category
- SKILL.md complete with all sections
- All examples tested and working
- No sensitive information
- No placeholder text
- Apache 2.0 license included
- Passes validation script
- Clear PR description

## License

All skills must be licensed under Apache License 2.0. Each skill directory must include:
1. A LICENSE file with full Apache 2.0 text
2. A license footer in SKILL.md
3. Current copyright year
