# A2A Integration Guide

This guide is the task-matched reference for the `a2a-engineer` role.

## What A2A Covers

A2A is the protocol layer for exposing an agent as a remote service. It
usually includes:

- an agent card or similar public capability descriptor
- request handlers for task intake and follow-up
- streaming updates for long-running work
- task lifecycle state transitions
- remote-agent client adapters
- auth, validation, and rate limiting

## When to Use It

Use the A2A role when the work is about:

- exposing an agent over a network protocol
- making an agent discoverable to remote callers
- handling task-based execution with progress updates
- integrating one agent with another agent or agent host
- building a standalone agentic service with a clear transport contract

Do not use this role for ordinary backend business logic, UI work, or model
prompt tuning unless the transport layer itself is the feature.

## Recommended Structure

Keep the transport layer small and explicit:

1. Agent card / capability metadata
2. Request handler / route wiring
3. Task store or persistence layer
4. Streaming output path
5. Remote client adapter
6. Tests that exercise the protocol end to end

Suggested module split:

- `agent_cards/` for public card definitions
- `transport/` for request handlers, task lifecycle, and streaming
- `clients/` for outbound remote-agent calls
- `config/` for protocol and runtime settings
- `tests/` for protocol-level validation

## Design Rules

- Treat the agent card as a public API contract.
- Keep protocol state transitions deterministic and observable.
- Prefer streaming updates for work that can take more than a few seconds.
- Keep remote-agent adapters thin so they can be replaced without rewriting the whole service.
- Put auth, validation, and timeouts at the edge.
- Log task starts, completions, failures, and cancellations with enough context to debug without leaking secrets.

## Runtime Checklist

- The card URL is reachable.
- The server binds to the declared port.
- The task endpoint accepts and validates input.
- Streaming emits progress before the final response.
- Cancellation and failure paths leave the task in a terminal state.
- Auth and rate limits apply before task execution.

## Testing Checklist

- Card discovery test
- Happy-path task execution test
- Streaming update test
- Failure-path task test
- Cancellation test
- Remote-agent compatibility test when the feature talks to another host

## Deployment Notes

- Keep transport configuration in environment variables.
- Make the card URL and host/port explicit in deployment docs.
- If the product uses containers, expose only the ports the protocol needs.
- If the agent service depends on another internal service, document the dependency in the product planning artifacts as well.
