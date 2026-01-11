# Claude Skills Library & Creator

A complete system for creating, organizing, and sharing Claude Code skills.

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-0-brightgreen.svg)](skills/)

## What Is This Repository?

This repository contains **two complementary parts**:

### 1. Skills Library (Main Directory)
📚 **A curated collection of ready-to-use Claude Code skills**
- Pre-made skills organized by category
- Ready to browse and use immediately
- Located in `skills/` directory

### 2. Skill Creator Tool (Subdirectory)
🛠️ **A toolkit for creating new skills**
- Interactive wizard with templates
- Validation and best practices
- Located in `claude-code-skill-creator/` subdirectory

---

## Quick Navigation

Choose your path:

### 🎯 I want to USE an existing skill
→ Browse the [`skills/`](skills/) directory by category
→ Each skill has a SKILL.md with complete instructions
→ [Getting Started Guide →](GETTING_STARTED.md)

### ✨ I want to CREATE a new skill
→ Use the creator tool in [`claude-code-skill-creator/`](claude-code-skill-creator/)
→ Interactive wizard makes it easy
→ [Creator Tool README →](claude-code-skill-creator/README.md)

### 🤝 I want to CONTRIBUTE a skill
→ Read the contribution guide
→ Submit via pull request
→ [Contributing Guide →](CONTRIBUTING.md)

---

## 📚 Available Skills

<!-- This section will auto-populate as you add skills -->

### Development
- *Coming soon*

### DevOps
- *Coming soon*

### Documentation
- *Coming soon*

### Automation
- *Coming soon*

## 🚀 Quick Start

### Using a Skill

1. Browse the [`skills/`](skills/) directory
2. Find a skill that matches your needs
3. Read the skill's `SKILL.md` for instructions
4. Follow the step-by-step guide

### Example

```bash
# Navigate to a skill directory
cd skills/git-commit-formatter

# Read the instructions
cat SKILL.md

# Follow the skill's steps
```

## 📖 Repository Structure

```
claude-skills-library/
├── README.md                 # This file
├── LICENSE                   # Apache 2.0 License
├── CONTRIBUTING.md           # How to contribute
├── SKILL_TEMPLATE.md         # Template for new skills
│
├── skills/                   # All skills organized by category
│   ├── development/
│   │   └── skill-name/
│   │       ├── SKILL.md      # Skill documentation
│   │       ├── scripts/      # Optional scripts
│   │       └── config/       # Optional config files
│   ├── devops/
│   ├── documentation/
│   └── automation/
│
├── docs/                     # Additional documentation
│   ├── SKILL_GUIDELINES.md   # Writing guidelines
│   └── CATEGORIES.md         # Category definitions
│
└── .github/                  # GitHub configuration
    ├── workflows/            # CI/CD automation
    └── ISSUE_TEMPLATE/       # Issue templates
```

## 🎯 Skill Categories

Skills are organized into the following categories:

- **development/** - Coding, testing, debugging tools
- **devops/** - Deployment, infrastructure, CI/CD
- **documentation/** - Writing, formatting, generation
- **automation/** - Scripting, task automation, workflows

See [docs/CATEGORIES.md](docs/CATEGORIES.md) for detailed category definitions.

## ✨ Contributing

We welcome contributions! Here's how to add a skill:

### Quick Contribution

1. **Fork this repository**
2. **Create a new skill directory**:
   ```bash
   mkdir -p skills/category-name/your-skill-name
   ```
3. **Copy the template**:
   ```bash
   cp SKILL_TEMPLATE.md skills/category-name/your-skill-name/SKILL.md
   ```
4. **Fill in the skill documentation**
5. **Add any scripts or config files**
6. **Test your skill thoroughly**
7. **Submit a pull request**

### Detailed Guide

See [CONTRIBUTING.md](CONTRIBUTING.md) for:
- Skill writing guidelines
- Quality standards
- Review process
- Style guide

## 📋 Skill Requirements

Every skill must include:

- [ ] **SKILL.md** - Complete documentation following the template
- [ ] **Clear category** - Placed in the correct category folder
- [ ] **Working examples** - Tested and verified
- [ ] **Prerequisites** - List all requirements
- [ ] **No sensitive data** - No API keys, passwords, etc.

Optional but recommended:
- [ ] **Scripts** - Automation helpers in `scripts/` folder
- [ ] **Config examples** - Sample configs in `config/` folder
- [ ] **Screenshots** - Visual aids where helpful
- [ ] **Tests** - Validation scripts

## 🔍 Finding Skills

### By Category
Browse the `skills/` directory by category.

### By Search
Use GitHub's search or:
```bash
# Search skill names
find skills -name "SKILL.md" | xargs grep -l "keyword"

# Search skill content
grep -r "keyword" skills/*/SKILL.md
```

### By Tags
Check skill metadata for tags (coming soon).

## 🛠️ Using the Skill Creator Tool

The skill creator toolkit is **included in this repository** at `claude-code-skill-creator/`:

```bash
# Navigate to the creator tool
cd claude-code-skill-creator

# Make scripts executable (first time only)
chmod +x scripts/*.sh

# Create a new skill using the wizard
./scripts/create-skill.sh

# The wizard will guide you through:
# 1. Naming your skill
# 2. Choosing a template
# 3. Generating files
# 4. Validating the skill

# Then move the completed skill to the library
mv your-skill-name ../skills/category-name/
```

See the [Skill Creator README](claude-code-skill-creator/README.md) for complete documentation.

## ✅ Validation

Before submitting, validate your skill:

```bash
# Using the built-in skill creator validator
./claude-code-skill-creator/scripts/validate-skill.sh skills/category/your-skill

# The validator checks:
# - SKILL.md exists and is complete
# - No {{PLACEHOLDER}} text remaining
# - Apache 2.0 license included
# - Balanced markdown code blocks
# - No TODO/FIXME markers
```

## 📜 License

All skills in this repository are licensed under the Apache License 2.0.

This means you can:
- ✅ Use commercially
- ✅ Modify freely
- ✅ Distribute
- ✅ Sublicense
- ❌ Hold liable
- ❌ Use trademark

See [LICENSE](LICENSE) for the full license text.

## 🙏 Contributors

Thanks to all contributors who have shared their skills!

<!-- Contributors will be automatically listed here -->

## 📞 Support

- **Questions**: Open a [Discussion](https://github.com/YOUR_USERNAME/claude-skills-library/discussions)
- **Issues**: Report [Issues](https://github.com/YOUR_USERNAME/claude-skills-library/issues)
- **New Skills**: Submit a [Pull Request](https://github.com/YOUR_USERNAME/claude-skills-library/pulls)

## 🗺️ Roadmap

- [ ] Reach 10 skills
- [ ] Add skill search functionality
- [ ] Create skill tags/metadata
- [ ] Add automated testing
- [ ] Build skill dependency tracking
- [ ] Create web interface for browsing

## 💡 Skill Ideas

Looking for inspiration? Check out our [skill ideas list](https://github.com/YOUR_USERNAME/claude-skills-library/issues?q=is%3Aissue+is%3Aopen+label%3Askill-idea).

Or suggest your own by opening an issue!

## 📊 Stats

- **Total Skills**: 0 (and growing!)
- **Categories**: 4
- **Contributors**: 1
- **Last Updated**: 2026-01-11

---

**Start exploring skills in the [`skills/`](skills/) directory!** 🚀
