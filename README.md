
# Documentation Repository for AI-Assisted Development

This repository stores comprehensive Markdown documentation designed to enhance AI agent code generation. By providing detailed, well-structured documentation, we enable AI assistants to produce more accurate and functional code with fewer generation iterations.

## Purpose

The primary goal is to create a knowledge base that helps AI agents understand requirements, patterns, and best practices, resulting in:

- Higher quality generated code
- Reduced iteration cycles
- Improved development efficiency
- Better alignment with project standards

## Contributing

I welcome community contributions! Please help us grow this documentation through:

- **Forks**: Create your own copy and customize as needed
- **Pull Requests**: Submit improvements, new documentation, or corrections

Your contributions make this resource more valuable for the entire community.

> [!IMPORTANT]
> **Commit Standards Required**: All pull requests **must** follow the **Conventional Commits** pattern.
> Commits that do not adhere to this standard will be rejected.

### Commit Message Format

```
<type>: <description>
```

**Types:**
| Type | Description |
|------|-------------|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation changes |
| `style` | Code formatting (no logic changes) |
| `refactor` | Code refactoring |
| `test` | Adding or modifying tests |
| `chore` | Build tasks, configs, dependencies |
| `perf` | Performance improvements |
| `ci` | CI/CD changes |

**Rules:**
- Use lowercase for the type
- Write description in imperative mood (e.g., "Add", "Fix", "Update")
- Keep the first line concise (ideally under 50 characters)
- No period at the end of the description

**Examples:**
- `feat: add user authentication`
- `fix: resolve login timeout issue`
- `docs: update installation guide`
- `refactor: simplify validation logic`

### Folder Structure

When adding new documentation, follow this folder structure pattern:

```
topic/
├── index.md              ← Main overview/quickstart
├── Section/
│   ├── index.md          ← Section overview
│   ├── feature-one.md
│   └── feature-two.md
└── AnotherSection/
    └── ...
```

**Conventions:**
| Element | Format | Example |
|---------|--------|---------|
| Folders | PascalCase | `BestPractices/`, `Multimodal/` |
| Files | kebab-case | `audio-input.md`, `prompt-caching.md` |
| Index files | `index.md` | Main entry point for each folder |

**Rules:**
- Group related documentation into folders
- Each folder should have an `index.md` as entry point
- Keep file names descriptive but concise
- Avoid flat structures with many files at the same level

## How to Use

Include references to relevant documentation when prompting AI agents to generate code. The more context provided, the better the results.

---

**Let's build better AI-assisted development together!**
