# Python / Streamlit Frontend Stack Pack

Use this pack for Streamlit-based Python frontend products.

## Stack Profile

- Framework: Streamlit
- Language: Python
- UI Model: page/app scripts with widgets and callbacks
- Styling: Streamlit native styling or the product-standard theme layer
- State: Streamlit session state or the product-standard app state pattern
- Testing: pytest-based UI or integration checks where supported

## Working Rules

- Keep UI code simple and explicit.
- Keep interactions close to the page script or module that owns them.
- Avoid over-abstracting widget state.
- Keep data fetch/update behavior easy to trace.

## Expected References

- `agents/frontend-developer/references/code-patterns.md`

## Notes

- This pack holds the Streamlit-specific assumptions that should not live in the base frontend skill.
