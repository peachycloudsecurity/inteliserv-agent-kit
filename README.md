# inteliserv-agent-kit

Persona and tool definitions for the InteliServ support agent, used by the
**OWASP Agentic Top 10 labs, ASI04 (Agentic Supply Chain)**:
https://github.com/peachycloudsecurity/owasp-agentic-ai-top-10

> Training repository. Some releases are **intentionally malicious** to show a
> supply chain compromise. The "malicious" content is only prompt text; there
> is no harmful code. Do not use this kit in a real product.

## Layout

```
agent_kit/persona.py   AGENT_NAME, GREETING, SYSTEM_PROMPT (plain strings)
agent_kit/tools.json   tool names, descriptions, parameters, permissions
```

## Releases

Every push to `main` that touches `agent_kit/` publishes the next patch
version (`v1.0.0`, `v1.0.1`, ...) as a GitHub Release and marks it **latest**
(`.github/workflows/release.yml`).

- `v1.0.0`: the reviewed, clean kit.
- Later versions: published after a (simulated) maintainer account compromise.

The lab pulls the **latest** release in attack mode, and only the pinned,
reviewed commit of `v1.0.0` in defense mode.
