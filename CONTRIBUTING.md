# Contributing to Insite Lab

First off, thanks for taking the time to contribute! ❤️

All types of contributions are encouraged and valued. See the [Table of Contents](#table-of-contents) for different ways to help and details about how this project handles them.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [I Have a Question](#i-have-a-question)
- [I Want to Contribute](#i-want-to-contribute)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Enhancements](#suggesting-enhancements)
- [Your First Code Contribution](#your-first-code-contribution)
- [Style Guides](#style-guides)
- [Commit Messages](#commit-messages)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## I Have a Question

> If you want to ask a question, we assume that you have read the available [Documentation](docs/).

Before you ask a question, it is best to search for existing [Issues](issues/) that might help you. In case you have found a suitable issue and still need clarification, you can write your question in this issue.

The best way to get your question answered is:

1. Join our [Discord community](https://discord.gg/insitelab)
2. Open a [Discussion](discussions)
3. Ask on [Twitter](https://twitter.com/insitelab)

## I Want to Contribute

> ### Legal Notice
> When contributing to this project, you must agree that you have authored 100% of the content, that you have the necessary rights to the content, and that the content you contribute may be provided under the project license.

### Reporting Bugs

#### Before Submitting a Bug Report

A good bug report shouldn't leave others needing to chase you up for more information. Therefore, we ask you to investigate carefully, collect information and describe the issue in detail in your report.

#### How Do I Submit a Good Bug Report?

We use GitHub issues to track bugs and errors. If you run into issues, please open an issue and include:

- Use a **clear and descriptive title** for the issue
- **Describe the exact steps** to reproduce the problem
- **Provide specific examples** to demonstrate the steps
- **Describe the behavior** you observed after running the steps
- **Explain which behavior** you expected to see instead and why
- **Include screenshots and animated GIFs** if possible

> **Note:** If you find a **Closed** issue that seems like it is the same thing that you're experiencing, open a new issue and include a link to the original issue.

### Suggesting Enhancements

Enhancement suggestions are tracked as [GitHub issues](issues/). Create an issue and provide:

- **Use a clear and descriptive title** for the issue
- **Provide a step-by-step description** of the suggested enhancement
- **Provide specific examples** to demonstrate the steps
- **Describe the current behavior** and **explain which behavior you expected to see instead**
- **Explain why this enhancement would be useful**

### Your First Code Contribution

Unsure where to begin contributing? You can start by looking through these `beginner` and `help-wanted` issues:

- [Beginner issues](https://github.com/Insite-lab/Insite-lab/labels/beginner) - issues which should only require a few lines of code
- [Help wanted issues](https://github.com/Insite-lab/Insite-lab/labels/help%20wanted) - issues which should be a bit more involved

#### Pull Request Process

1. Fork the repository
2. Create a new branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Run the tests (`npm test` or equivalent)
5. Commit your changes using conventional commits (see below)
6. Push to your fork (`git push origin feature/amazing-feature`)
7. Open a Pull Request

## Style Guides

### Code Style

All code should follow the style guides defined in each repository. Common conventions:

- **JavaScript/TypeScript**: ESLint + Prettier
- **Python**: Black + isort + flake8
- **Go**: gofmt
- **Rust**: rustfmt

### Commit Messages

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

**Types:**

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that do not affect the meaning of the code
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `perf`: A code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `chore`: Changes to the build process or auxiliary tools

**Examples:**

```
feat(api): add user authentication endpoint

Add POST /api/v1/auth/login endpoint with JWT token generation.

Closes #123
```

```
docs(readme): update installation instructions
```

## License

By contributing, you agree that your contributions will be licensed under the project's LICENSE file.

---

Thank you for contributing to Insite Lab! 🚀
