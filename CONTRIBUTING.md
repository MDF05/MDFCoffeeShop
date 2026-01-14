# Contributing to CoffeShop

Thank you for your interest in contributing to **CoffeShop**! While this is a proprietary project, we welcome internal contributions and bug reports from approved collaborators.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Pull Request Process](#pull-request-process)
- [Coding Standards](#coding-standards)

## 🤝 Code of Conduct

This project and everyone participating in it is governed by the [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## 🚀 Getting Started

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/coffeshop.git
    ```
2.  **Install dependencies**:
    ```bash
    npm install
    ```
3.  **Set up environment variables**:
    Copy `.env.example` to `.env` and configure the necessary keys (see [ENVIRONMENT.md](ENVIRONMENT.md)).

## 🛠 Development Workflow

### Branching Strategy

We follow a simplified Gitflow workflow:

- **`main`**: The stable, production-ready branch.
- **`develop`**: The main integration branch for the next release.
- **`feature/feature-name`**: Branches for new features, created from `develop`.
- **`bugfix/issue-description`**: Branches for bug fixes, created from `develop`.
- **`hotfix/issue-description`**: Branches for critical production fixes, created from `main`.

### Commit Messages

We use [Conventional Commits](https://www.conventionalcommits.org/):

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that do not affect the meaning of the code (white-space, formatting, etc)
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `test`: Adding missing tests or correcting existing tests
- `chore`: Changes to the build process or auxiliary tools

**Example**:
```
feat(auth): implement user login screen
```

## 📥 Pull Request Process

1.  Ensure your code builds and runs locally with no errors.
2.  Update the documentation if you changed any functionality.
3.  Run the test suite and ensure all tests pass (`npm test`).
4.  Open a Pull Request (PR) against the `develop` branch.
5.  Provide a clear description of the changes and link to any relevant issues.
6.  Request a review from a team member.

## 🎨 Coding Standards

Please refer to the [Style Guide](STYLE_GUIDE.md) for detailed information on our coding conventions, linting rules, and formatting preferences.
