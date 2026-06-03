# htmx Frontend Stack Pack

Use this pack for server-driven HTML products that use htmx.

## Stack Profile

- UI Model: server-rendered HTML with incremental fragment updates
- Interactivity: htmx-driven swaps, requests, and partial refreshes
- Styling: product-standard CSS or utility classes
- State: server-side session/request state, not heavy client state
- Testing: integration and browser checks for HTML fragment behavior

## Working Rules

- Keep the server as the source of truth for view state.
- Keep fragments small and reusable.
- Keep request targets, swap targets, and response shapes explicit.
- Avoid building React-style client-side architecture on top of htmx.

## Expected References

- `agents/frontend-developer/references/code-patterns.md`

## Notes

- This pack holds the htmx-specific assumptions that should not live in the base frontend skill.
