# Start Here - Quick Decision Guide

New to this repository? This guide will help you find exactly what you need.

## Understanding This Repository

This repository is organized as **two complementary parts**:

### 📚 The Library (Books)
A collection of ready-to-use skills organized by category in the `skills/` directory.
**Think of it as:** The library of books you can read and use.

### 🛠️ The Creator Tool (Printing Press)
A toolkit for creating new skills with templates and validation in the `claude-code-skill-creator/` directory.
**Think of it as:** The printing press that helps you write and publish new books.

---

## What Do You Want to Do?

### Option 1: USE an Existing Skill 📖

**You want to:** Find and follow instructions for a specific task

**Go to:** [`skills/`](skills/) directory

**Steps:**
1. Browse by category:
   - [`development/`](skills/development/) - Code-related skills
   - [`devops/`](skills/devops/) - Infrastructure & deployment
   - [`documentation/`](skills/documentation/) - Documentation creation
   - [`automation/`](skills/automation/) - Task automation
2. Open a skill directory
3. Read the `SKILL.md` file
4. Follow the instructions

**Documentation:** [GETTING_STARTED.md](GETTING_STARTED.md)

---

### Option 2: CREATE a New Skill ✍️

**You want to:** Make a new skill from scratch

**Go to:** [`claude-code-skill-creator/`](claude-code-skill-creator/) directory

**Steps:**
1. Navigate to the creator tool:
   ```bash
   cd claude-code-skill-creator
   ```
2. Make scripts executable (first time only):
   ```bash
   chmod +x scripts/*.sh
   ```
3. Run the interactive wizard:
   ```bash
   ./scripts/create-skill.sh
   ```
4. Follow the prompts to create your skill
5. Move the completed skill to the library:
   ```bash
   mv your-skill-name ../skills/category-name/
   ```

**Documentation:** [claude-code-skill-creator/README.md](claude-code-skill-creator/README.md)

---

### Option 3: CONTRIBUTE a Skill to the Library 🤝

**You want to:** Share a skill with others via pull request

**Go to:** [CONTRIBUTING.md](CONTRIBUTING.md)

**Steps:**
1. Fork this repository
2. Create your skill (using Option 2 above, or manually)
3. Place it in the appropriate `skills/category/` directory
4. Validate your skill:
   ```bash
   ./claude-code-skill-creator/scripts/validate-skill.sh skills/category/your-skill
   ```
5. Create a pull request with commit message:
   ```bash
   git checkout -b skill/your-skill-name
   git add skills/category/your-skill-name/
   git commit -m "feat(category): add your-skill-name"
   git push origin skill/your-skill-name
   ```

**Documentation:** [CONTRIBUTING.md](CONTRIBUTING.md)

---

### Option 4: IMPROVE the Creator Tool 🔧

**You want to:** Enhance the skill creation toolkit itself

**Go to:** [`claude-code-skill-creator/CONTRIBUTING.md`](claude-code-skill-creator/CONTRIBUTING.md)

**This is for:**
- Adding new templates
- Improving validation
- Fixing bugs in scripts
- Enhancing the wizard

**Documentation:** [claude-code-skill-creator/CONTRIBUTING.md](claude-code-skill-creator/CONTRIBUTING.md)

---

### Option 5: UNDERSTAND the Project 🧠

**You want to:** Learn about the architecture and design

**Read these in order:**
1. [README.md](README.md) - Project overview
2. [CLAUDE.md](CLAUDE.md) - Technical architecture and guidance
3. [docs/CATEGORIES.md](docs/CATEGORIES.md) - Category system explained
4. [docs/SKILL_GUIDELINES.md](docs/SKILL_GUIDELINES.md) - Writing guidelines

---

## Still Confused?

### Common Questions

**Q: What's the difference between the library and the creator tool?**
- **Library** (`skills/`) = Collection of completed skills you can use
- **Creator Tool** (`claude-code-skill-creator/`) = Tool to help you create new skills

**Q: Can I use the creator tool standalone?**
- Yes! The creator tool works independently. You can use it to create skills for your own use without contributing to this library.

**Q: Do I need to use the creator tool to contribute?**
- No, but it's recommended. You can manually create skills using the [SKILL_TEMPLATE.md](SKILL_TEMPLATE.md) template.

**Q: Where do I find example skills?**
- Check [`skills/`](skills/) for skills in the library
- Check [`claude-code-skill-creator/examples/`](claude-code-skill-creator/examples/) for example skills created with the tool

**Q: How do I know which category to use?**
- See [docs/CATEGORIES.md](docs/CATEGORIES.md) for a decision tree and detailed category descriptions.

---

## Quick Links

### For Users (Reading Books)
- [Browse Skills →](skills/)
- [Getting Started →](GETTING_STARTED.md)
- [Quick Reference →](QUICK_REFERENCE.md)

### For Creators (Writing Books)
- [Skill Creator Tool →](claude-code-skill-creator/)
- [Skill Template →](SKILL_TEMPLATE.md)
- [Writing Guidelines →](docs/SKILL_GUIDELINES.md)

### For Contributors (Publishing Books)
- [How to Contribute →](CONTRIBUTING.md)
- [Category Guide →](docs/CATEGORIES.md)
- [Validation Tool →](claude-code-skill-creator/scripts/validate-skill.sh)

---

## Next Steps

1. **Pick an option above** that matches what you want to do
2. **Follow the steps** provided for that option
3. **Read the linked documentation** for more details
4. **Ask for help** if you get stuck (open a [Discussion](https://github.com/YOUR_USERNAME/claude-skills/discussions))

Happy skill building! 🚀
