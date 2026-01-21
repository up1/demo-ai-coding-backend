---
agent: agent
description: This prompt is used to add changes and create git commit messages with conventional commits.
---

Steps to implement Git Flow:
1. Generate a concise and descriptive commit message following the Conventional Commits specification.
2. Stage all changes using `git add .`.
3. Create a commit with the generated message using `git commit -m "<commit-message>".
4. Ensure the commit message adheres to the Conventional Commits format, such as:
   - feat: for new features
   - fix: for bug fixes
   - docs: for documentation changes
   - style: for code style changes (formatting, missing semicolons, etc.)
   - refactor: for code refactoring without changing functionality
   - test: for adding or updating tests
   - chore: for maintenance tasks and other changes that don't modify src or test files

5. Return the git commands executed along with the commit message.

Example output:
```git add .
git commit -m "feat: add user authentication module"```

Make sure to replace the example commit message with one that accurately reflects the changes made in the codebase.

6. Create PR(Pull Request) description based on the commit messages if multiple commits are made.

Example PR description:
```### Summary
This PR introduces the following changes:
- feat: add user authentication module
- fix: resolve issue with data validation in user registration
- docs: update API documentation for new endpoints
### Related Issues
- Closes #123
- Closes #124
### Checklist
- [x] My code follows the style guidelines of this project
- [x] I have performed a self-review of my code
- [x] I have commented my code, particularly in hard-to-understand areas
- [x] I have made corresponding changes to the documentation
- [x] My changes generate no new warnings
- [x] I have added tests that prove my fix is effective or that my feature works
- [x] New and existing unit tests pass locally with my changes``` 

Remember to follow best practices for commit messages, keeping them clear and informative.