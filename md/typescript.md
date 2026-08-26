## TypeScript

- Prefer optional chaining (`?.`) for null-safe property and method access.  
  Don’t mix `obj?.x` with `obj.x && ...` in the same access path:

  ```typescript
  // Good
  const includesPattern = obj?.field?.includes("pattern");

  // Bad
  const includesPattern = obj?.field && obj.field.includes("pattern");
  ```

- Use dot notation for field access. Bracket notation only for dynamic keys or special characters:

  ```ts
  // Good
  user.name;
  obj[dynamicKey];

  // Bad
  user["name"];
  ```

- Always use curly braces for control flow blocks, even single-line:

  ```ts
  // Good
  if (condition) {
    doSomething();
  }

  // Bad
  if (condition) doSomething();
  ```

- Use a named options object for functions with 3+ parameters:

  ```ts
  type GetUserOptions = { userId: string; includeProfile: boolean; locale: string };
  async function getUser(options: GetUserOptions): Promise<User> { ... }
  ```

- Inline `Promise.all` calls when they're simple and readable. Extract to named variables when calls have many arguments or are hard to read inline.
- File order: constants → exports → private helpers (in order of first use).
- Mirror source structure for test files: `src/users/service.ts` → `test/users/service.test.ts`
- Use `type` for data structures.
- Use `class` for behavior/state.
- Use `interface` only when necessary.
- Prefer named functions over arrow functions (except inline callbacks).
