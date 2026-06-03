# Vue 3 + Vite + TypeScript Best Practices

This stack pack applies when the product declares a Vue frontend, typically under `{PRODUCT_ROOT}/portal/`.

## Scope

- Use Vue 3 composition API and `<script setup lang="ts">`
- Use Vite for both dev server and production build
- Use TypeScript for props, emits, composables, and API DTOs
- Use Vue Router for page routing and Pinia for shared client state when needed
- Keep UI logic feature-local unless a shared primitive is genuinely reusable

## Routing and Layout

- Keep route definitions centralized in the product router
- Keep app shell, sidebar, header, and auth gate logic separate from page modules
- Prefer page-level composition with feature-local components under the declared portal root

## Forms and Validation

- Prefer schema-aligned validation when the backend exposes shared contracts
- Keep form state explicit and minimize implicit cross-component coupling
- Use typed composables for repeated form or API behaviors

## API and Data Flow

- Keep API clients in a dedicated infrastructure layer
- Normalize backend responses at the edge instead of spreading mapping logic through pages
- Treat loading, empty, and error states as first-class UI states

## Testing

- Use Vitest for unit tests and component tests
- Add route-level coverage for portal entrypoints and major workflow pages
- Keep mocks close to the feature slice they support

## Docker / Runtime Notes

- Build the app with `npm run build`
- Serve the generated `dist/` directory behind Nginx or another static file server
- Keep the portal root path, base path, and API base URL aligned in config

