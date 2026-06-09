```markdown
# gaokaomath Development Patterns

> Auto-generated skill from repository analysis

## Overview
The `gaokaomath` repository is a TypeScript codebase focused on mathematical logic, likely for educational or examination purposes (e.g., Gaokao math). This skill teaches you the project's coding conventions, file organization, and testing patterns to ensure consistency and maintainability across contributions.

## Coding Conventions

### File Naming
- Use **snake_case** for all file names.
  - Example: `math_utils.ts`, `problem_solver.ts`

### Imports
- Use **relative import paths** for internal modules.
  - Example:
    ```typescript
    import { solveEquation } from './equation_solver';
    ```

### Exports
- Use **named exports** exclusively.
  - Example:
    ```typescript
    // In math_utils.ts
    export function add(a: number, b: number): number {
      return a + b;
    }
    ```

### Commit Messages
- Commit messages are **freeform** (no enforced prefix), averaging around 71 characters.
  - Example:
    ```
    Add quadratic equation solver and update documentation
    ```

## Workflows

### Adding a New Module
**Trigger:** When you need to introduce new functionality.
**Command:** `/add-module`

1. Create a new file using snake_case (e.g., `new_feature.ts`).
2. Implement your logic using TypeScript.
3. Use named exports for all functions or constants.
4. Import dependencies using relative paths.
5. Write a corresponding test file (see Testing Patterns).
6. Commit with a clear, descriptive message.

### Updating an Existing Module
**Trigger:** When modifying or extending existing logic.
**Command:** `/update-module`

1. Locate the relevant file (e.g., `math_utils.ts`).
2. Make your changes, following the code style conventions.
3. Update or add tests as needed.
4. Commit with a descriptive message.

### Running Tests
**Trigger:** To verify code correctness.
**Command:** `/run-tests`

1. Identify test files matching the `*.test.*` pattern.
2. Use the project's test runner (framework not detected; check project docs or package.json).
3. Run all tests and ensure they pass before committing changes.

## Testing Patterns

- Test files follow the `*.test.*` naming convention (e.g., `math_utils.test.ts`).
- The testing framework is **unknown** (not detected in analysis).
- Place tests alongside or near the modules they test.
- Example test file structure:
  ```typescript
  // math_utils.test.ts
  import { add } from './math_utils';

  describe('add', () => {
    it('adds two numbers', () => {
      expect(add(2, 3)).toBe(5);
    });
  });
  ```

## Commands
| Command        | Purpose                                      |
|----------------|----------------------------------------------|
| /add-module    | Scaffold a new module with tests             |
| /update-module | Update an existing module and its tests       |
| /run-tests     | Run all test files in the repository          |
```
