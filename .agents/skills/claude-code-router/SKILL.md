```markdown
# claude-code-router Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `claude-code-router` TypeScript codebase. You'll learn how to structure files, write imports and exports, and follow commit and testing conventions. This guide ensures consistency and maintainability across the project.

## Coding Conventions

### File Naming
- Use **kebab-case** for all filenames.
  - Example: `router-handler.ts`, `user-service.ts`

### Import Style
- Use **relative imports** for all modules.
  - Example:
    ```typescript
    import { handleRoute } from './router-handler';
    ```

### Export Style
- Use **named exports** exclusively.
  - Example:
    ```typescript
    // router-handler.ts
    export function handleRoute(req, res) { ... }
    ```

### Commit Patterns
- Commit messages are **freeform** with no strict prefix requirements.
- Average commit message length is around 31 characters.
  - Example:  
    ```
    Add basic routing logic
    ```

## Workflows

### Adding a New Router Handler
**Trigger:** When you need to add a new route handler to the project  
**Command:** `/add-router-handler`

1. Create a new file in kebab-case (e.g., `new-route-handler.ts`).
2. Implement the handler function and use a named export.
    ```typescript
    export function newRouteHandler(req, res) { ... }
    ```
3. Import the handler in the relevant module using a relative path.
    ```typescript
    import { newRouteHandler } from './new-route-handler';
    ```
4. Add any necessary tests in a corresponding `*.test.ts` file.

### Writing and Running Tests
**Trigger:** When you need to verify the functionality of your code  
**Command:** `/run-tests`

1. Create a test file with the `.test.ts` suffix (e.g., `router-handler.test.ts`).
2. Write your tests using the project's preferred (undetected) testing framework.
3. Run the tests using the project's test runner (framework not specified; check project documentation or package scripts).

## Testing Patterns

- Test files are named using the `*.test.ts` pattern and are placed alongside the modules they test.
- The specific testing framework is **unknown**; refer to project scripts or documentation for details.
- Example test file:
    ```typescript
    // router-handler.test.ts
    import { handleRoute } from './router-handler';

    describe('handleRoute', () => {
      it('should process the request', () => {
        // test implementation
      });
    });
    ```

## Commands

| Command              | Purpose                                      |
|----------------------|----------------------------------------------|
| /add-router-handler  | Scaffold a new router handler module         |
| /run-tests           | Run all test files in the project            |
```
