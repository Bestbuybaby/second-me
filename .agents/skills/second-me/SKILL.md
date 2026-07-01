```markdown
# second-me Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides guidance on the development patterns and conventions used in the `second-me` TypeScript codebase. It covers file organization, code style, commit practices, and testing approaches to ensure consistency and maintainability throughout the project.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `messageHandler.test.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { getUser } from './userProfile';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // userProfile.ts
    export function getUser(id: string) { /* ... */ }
    export const USER_ROLE = 'admin';
    ```

### Commit Messages
- Follow **Conventional Commits** with the `build` prefix.
  - Example:
    ```
    build: update dependencies to latest versions
    ```

## Workflows

### Build Workflow
**Trigger:** When you need to update or manage build dependencies or configurations.
**Command:** `/build`

1. Make necessary changes to build scripts or dependencies.
2. Commit your changes using the `build:` prefix in the commit message.
   - Example: `build: upgrade TypeScript to 4.9.5`
3. Push your changes to the repository.

## Testing Patterns

- Test files follow the `*.test.*` naming convention.
  - Example: `userProfile.test.ts`
- The testing framework is not explicitly specified; ensure tests are colocated with the code they verify and follow the naming pattern.
- Example test file:
  ```typescript
  // userProfile.test.ts
  import { getUser } from './userProfile';

  describe('getUser', () => {
    it('returns user data for valid id', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command  | Purpose                                         |
|----------|-------------------------------------------------|
| /build   | Run the build workflow for dependencies/configs  |
```
