# Nebula Adapter Compatibility Guide

Use this reference when the framework needs to adapt to a product that does not follow the default `engine/`, `experience/`, `neuron/` layout or when a stack-specific reference pack needs explicit routing.

## When to Use This Role

- The product declares `portal/`, `api/`, `services/`, or another non-default root in `BLUEPRINT.md`
- A Java / Spring Boot backend needs its own DevOps guidance
- A new stack pack or compatibility note would otherwise be hidden inside generic docs
- Framework docs need to be updated without touching product implementation code

## Required Behavior

- Keep generic framework docs generic
- Put stack-specific instructions in stack-specific reference packs
- Route users to the correct reference file in `ROUTER.md`
- Reflect the declared layout in `AGENT-USE.md`, `CONTAINER-STRATEGY.md`, and `blueprint-setup/README.md`

## Review Checklist

- The new stack or layout is named explicitly
- The router points at the correct reference file
- The compatibility guidance does not introduce product scope
- Any new folder names are mirrored in the blueprint and code index

