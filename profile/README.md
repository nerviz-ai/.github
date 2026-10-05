<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/nerviz-ai/nerviz/main/brand/nerviz-banner-dark.png">
    <img alt="Nerviz — an agent harness for Spring Boot" src="https://raw.githubusercontent.com/nerviz-ai/nerviz/main/brand/nerviz-banner-light.png" width="100%">
  </picture>
</p>

**Nerviz is an agent harness for Spring Boot on Claude Code.** It generates the project
from an architecture declared as data, designs every feature as an approved spec before any
code is written, and blocks at write time what that architecture forbids.

- **Architecture is data.** Seven blueprints — hexagonal, clean architecture, layered,
  onion, vertical slice, modular monolith — plus your own, each a YAML file.
- **Spec before code.** `/new-feature` designs one use case per run, layer by layer, and
  only an approved spec reaches the agent that writes `src/`.
- **Enforced, not promised.** Hooks refuse a write outside a skill's territory or a
  forbidden import, and ArchUnit and the build check the rest.
- **Self-contained.** A generated project carries the whole harness and updates itself
  with `/arch-adopt`.

## Repositories

| Repository | What it is |
|---|---|
| [`nerviz`](https://github.com/nerviz-ai/nerviz) | The harness: norms, skills, agents, blueprints and the `ArchHook` hooks. Start here. |
| [`marketplace`](https://github.com/nerviz-ai/marketplace) | Claude Code marketplace with `/arch-adopt`, which installs or updates Nerviz inside an existing Spring Boot project. |

## Get started

New project — follow [Getting started](https://github.com/nerviz-ai/nerviz#getting-started).
Existing project — install from the marketplace:

```bash
claude plugin marketplace add nerviz-ai/marketplace
claude plugin install nerviz@nerviz
```

Then run `/nerviz:arch-adopt` inside the project.

Documentation in [English](https://github.com/nerviz-ai/nerviz/blob/main/docs/en/README.md)
and [português](https://github.com/nerviz-ai/nerviz/blob/main/docs/pt-br/README.md).

## Contact

- Questions and ideas: [Discussions](https://github.com/nerviz-ai/nerviz/discussions)
- Security: [report privately](https://github.com/nerviz-ai/nerviz/security/advisories/new) or `security@nerviz.dev`
- Everything else: `hello@nerviz.dev`
- Support the project: [GitHub Sponsors](https://github.com/sponsors/ice-lfernandes)

<sub>Nerviz is pronounced *NAIR-viz*, after Pier Luigi Nervi. Not affiliated with
Anthropic, Broadcom or Oracle; Claude Code, Spring and Java are named only to describe what
Nerviz works with.</sub>
