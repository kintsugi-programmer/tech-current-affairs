# Spec-Driven Development: Coding with Clarity

Building apps today is changing. Writing and reviewing code used to be the hardest part. Now it's knowing how to tell an LLM what you want. That skill is **spec-driven development**.

## Vibe Coding vs Traditional SDLC

**Vibe coding** is what most people think of with AI coding agents:
- Start with a prompt (e.g., "build a login page in Python")
- AI generates boilerplate
- Edit prompt, regenerate, repeat until it works
- No planning phase — the LLM guesses the implementation each time

This skips the **Software Development Lifecycle (SDLC)**. Traditional SDLC goes: Plan → Design → Implement → Test → Deploy → Maintain. Vibe coding jumps straight to implementation, which means every run can produce different results.

## What is Spec-Driven Development?

Spec-driven development (spec coding) adds SDLC structure to AI-generated software. Instead of prompting an implementation, you prompt:

- **Behavior** — what the system should do
- **Constraints** — rules and boundaries

These become a **requirements specification** — a contract that guides all downstream work: code, tests, docs, verification.

### The Flow

1. **Prompt** → requirements spec (behavior + constraints)
2. **Approve/Edit** spec — nothing is built yet
3. **Design doc** with implementation to-dos
4. **AI agent implements** code from the design
5. **Generate tests** from the same spec

## How It Differs

| Approach | Start with | Strength |
|---|---|---|
| Traditional dev | Code | Intuition-driven |
| Test-driven dev (TDD) | Tests | Behavior-first |
| Spec-driven dev (SDD) | Specification | Contract-first |

SDD is like TDD on steroids — the spec becomes the primary artifact driving implementation, tests, and verification.

## Example: User Authentication

### Vibe Coding
- Prompt: "build a /login endpoint"
- AI guesses the structure — libraries, error handling, validation
- Back-and-forth edits until it works

### Spec-Driven
1. Define the feature: **User Authentication**
2. Specify behavior: "POST /login endpoint accepting `user` and `pass` variables"
3. Specify failure conditions: "return error if username is missing"
4. Generate test cases: "valid credentials → 200 response"
5. AI implements from the spec

The key difference: less ambiguity. The LLM knows *why* it's making decisions, and every implementation matches a shared contract.

## Why It Matters

- Removes ambiguity from AI coding
- Produces consistent, repeatable results
- Documents intent (not just code)
- Works across implementation, testing, and verification
