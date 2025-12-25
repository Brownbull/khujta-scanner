# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Purpose

This is a QA/testing project that uses Claude Code and the Claude Code Chrome extension to test web applications in development. The workflow involves:

1. Receiving context about an application to test
2. Navigating and interacting with the application as different user types
3. Identifying issues, broken workflows, and UX problems
4. Generating reports from the end-user perspective

## Testing Approach

When testing an application:
- Think from the user's perspective, not a developer's
- Test as different user personas (new user, power user, admin, etc.)
- Focus on workflows, not individual features in isolation
- Document issues in terms of user impact
- Note confusing UX, broken flows, and edge cases

## Report Format

When generating reports, include:
- What the user was trying to accomplish
- Steps taken
- Expected vs actual behavior
- Severity (blocker, major, minor, cosmetic)
- Screenshots or descriptions of the visual state when relevant

## Permissions

This project has restricted bash permissions configured in `.claude/settings.local.json`. Only directory listing, PowerShell commands, and cat commands are allowed by default.
