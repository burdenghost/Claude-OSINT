# ChatGPT OSINT adapter

The repository now includes `skills/chatgpt-osint/SKILL.md`.

## What it does

The adapter translates the repository's existing methodology and technical reference into a workflow suitable for ChatGPT. It uses available web/GitHub/files/connected tools rather than pretending that local CLI commands were executed.

It is designed for:
- authorized OSINT;
- passive external reconnaissance;
- defensive website and repository review;
- evidence correlation;
- structured security reporting.

It does not enable exploitation, credential use, destructive testing, authentication bypass, or evasion.

## ChatGPT Skills

OpenAI documents `SKILL.md` as the portable format for reusable skills. Eligible ChatGPT workspaces can upload a skill from the Skills interface. See the official OpenAI Skills documentation for current availability and installation instructions.

For OpenAI API/Agents environments, the same Agent Skills format can be uploaded as a versioned skill bundle.

## Current repository layout

- `skills/osint-methodology/SKILL.md` — analytical methodology.
- `skills/offensive-osint/SKILL.md` — technical reference catalog.
- `skills/chatgpt-osint/SKILL.md` — ChatGPT execution adapter.

## Important

Adding the adapter to GitHub does not automatically install it into a ChatGPT account. ChatGPT account/workspace installation is controlled by the ChatGPT Skills surface and account eligibility.