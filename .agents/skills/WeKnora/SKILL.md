```markdown
# WeKnora Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the WeKnora TypeScript codebase. It covers file naming, import/export styles, commit message conventions, and testing patterns. By following these guidelines, contributors can write consistent, maintainable code and collaborate effectively.

## Coding Conventions

### File Naming
- Use **PascalCase** for all file names.
  - **Example:** `UserProfile.ts`, `DataService.ts`

### Import Style
- Use **relative imports** for referencing other modules.
  - **Example:**
    ```typescript
    import { UserService } from './UserService';
    ```

### Export Style
- Use **named exports** exclusively.
  - **Example:**
    ```typescript
    export function fetchData() { ... }
    export const API_URL = '...';
    ```

### Commit Message Conventions
- Use **conventional commit** format.
- Prefixes observed: `refactor`
- Example message:
  ```
  refactor: update UserProfile to use new API endpoint
  ```

## Workflows

### Refactoring Code
**Trigger:** When improving code structure or updating logic without changing external behavior.
**Command:** `/refactor`

1. Identify the code that needs refactoring.
2. Make changes using PascalCase file names, relative imports, and named exports.
3. Write a commit message starting with `refactor:`, followed by a concise description.
4. Run tests to ensure nothing is broken.
5. Push your changes and open a pull request.

## Testing Patterns

- Test files use the pattern: `*.test.*` (e.g., `UserService.test.ts`)
- Testing framework is **unknown**; check existing test files for structure.
- Place tests alongside the modules they test or in a dedicated test directory.
- Example test file:
  ```typescript
  // UserService.test.ts
  import { getUser } from './UserService';

  describe('getUser', () => {
    it('returns user data for valid ID', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command     | Purpose                                      |
|-------------|----------------------------------------------|
| /refactor   | Start a refactoring workflow                 |
```
