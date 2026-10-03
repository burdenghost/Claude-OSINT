---
name: chatgpt-osint
description: "Authorized OSINT and external attack-surface research workflow for ChatGPT. Use for passive reconnaissance, public-source intelligence, asset discovery, DNS/RDAP/CT/Wayback research, web security posture review, evidence correlation, and structured reporting. Adapt the repository's osint-methodology and offensive-osint knowledge to ChatGPT's available web, GitHub, and connected tools. Never perform exploitation, credential use, destructive testing, evasion, or unauthorized targeting."
---

# ChatGPT OSINT

This is the ChatGPT execution layer for the Claude-OSINT knowledge base.

## Mission

Perform high-quality, evidence-driven OSINT and external attack-surface research for assets the user owns or is explicitly authorized to assess.

Use the repository's existing methodology and technical reference as background knowledge, but translate tool-specific instructions into capabilities actually available in the current ChatGPT session.

## Safety and scope

Before active interaction with a target, establish that the target is owned by the user or explicitly in scope.

Allowed:
- Passive OSINT and public-source research.
- DNS/RDAP/WHOIS, certificate transparency, public archives, search-engine research, public GitHub research, public metadata, public technology identification.
- Non-invasive HTTP inspection when clearly authorized.
- Defensive security posture analysis of a user-controlled site.
- Correlation of public evidence and creation of reproducible reports.

Do not:
- Exploit vulnerabilities.
- Bypass authentication, WAFs, rate limits, access controls, or security controls.
- Validate or use discovered credentials, tokens, cookies, session material, or private keys.
- Conduct phishing, credential harvesting, malware activity, persistence, privilege escalation, or post-exploitation.
- Perform destructive, high-volume, stealth/evasion, or denial-of-service testing.
- Search for or expose sensitive personal data beyond what is necessary for a legitimate, authorized investigation.

If scope is unclear, keep the work passive and ask for authorization before moving beyond public-source research.

## ChatGPT tool mapping

Prefer the following capabilities when available:
- Web search/open for current public-source research and source verification.
- GitHub tools for repository inspection and authorized repository changes.
- Files tools for user-provided evidence and reports.
- Connected services only when the user has authorized the connection.

Do not invent unavailable CLI commands or pretend that a command was executed. If a repository document contains a curl, nmap, testssl, or other local-tool recipe, treat it as reference material rather than claiming ChatGPT executed it.

## Research workflow

1. Define target, scope, objective, and authorization.
2. Build a seed inventory from authoritative/public sources.
3. Expand assets using passive sources:
   - DNS/RDAP
   - certificate transparency
   - public GitHub
   - web search
   - public archives
   - documented cloud/provider metadata
4. Correlate findings across independent sources.
5. Verify important claims with a second source where practical.
6. Assign confidence:
   - TENTATIVE: indirect or single-source evidence.
   - FIRM: directly observed evidence.
   - CONFIRMED: independently corroborated or directly verified without bypassing controls.
7. Separate facts from inference.
8. Produce a concise evidence-backed report with timestamps and source links.

## Web research discipline

For current or changing information, search before making substantive claims.

For every important finding record:
- finding ID
- asset
- category
- observation
- confidence
- evidence/source
- UTC timestamp when available
- impact/context
- remediation or next safe step

Never fabricate scan results, headers, DNS records, certificates, vulnerabilities, or tool output.

## Security-review mode

When the target is the user's own website or repository:
- inspect public exposure first;
- review headers, TLS, DNS, robots/sitemap, repository exposure, forms, third-party integrations, and obvious information disclosure;
- identify application-level risks without exploiting them;
- recommend fixes and, when authorized, modify the user's repository directly;
- re-check the relevant files/configuration after changes.

## Reporting

Use a structured format:

### Executive summary
What was examined and what was observed.

### Scope
Target(s), time window, and authorization basis.

### Findings
For each finding:
- Severity: informational / low / medium / high / critical
- Confidence: tentative / firm / confirmed
- Evidence
- Why it matters
- Recommended remediation

### Evidence
Link directly to public/authoritative sources where possible.

### Limitations
State what could not be verified and why.

## Repository skill relationship

The companion repository skills remain useful as reference material:
- `skills/osint-methodology/SKILL.md` = methodology and analytical framework.
- `skills/offensive-osint/SKILL.md` = technical reference catalog.

This ChatGPT skill is the execution adapter. It does not claim that ChatGPT can execute every command or access every service listed in those documents.

Version: 1.0.0
