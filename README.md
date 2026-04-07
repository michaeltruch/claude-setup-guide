# Claude Code Setup Guide

Mein komplettes Claude Code Setup: Skills, Plugins, MCP-Server und Tools.

## Inhaltsverzeichnis

- [Skills (claude.ai)](#skills-claudeai)
- [Plugins (Claude Code)](#plugins-claude-code)
- [MCP-Server (Integrationen)](#mcp-server-integrationen)
- [gstack (Garry Tan's Engineering Stack)](#gstack)
- [Installation](#installation)
- [Nutzungsbeispiele](#nutzungsbeispiele)

---

## Skills (claude.ai)

Skills sind prompt-basierte Erweiterungen, die in claude.ai unter **Anpassen > Skills** verwaltet werden.

| Skill | Beschreibung | Anwendungsfall |
|---|---|---|
| `/app-builder-pro` | Strukturierter Build-Workflow mit Code-Review & Logic Validation | Apps bauen (React, Node.js, Full-Stack, CLI) |
| `/skill-creator` | Skills erstellen, verbessern und Performance messen | Neue Skills entwickeln |
| `/canvas-design` | Visuelle Kunst als .png/.pdf mit Design-Philosophie | Poster, Designs, visuelle Kunst erstellen |
| `/web-artifacts-builder` | Multi-Component HTML Artifacts mit React, Tailwind, shadcn/ui | Komplexe Web-Artifacts bauen |
| `/mcp-builder` | MCP Server Development Guide (Python/TypeScript) | Externe APIs anbinden |
| `/theme-factory` | 10 vorgefertigte Themes (Farben/Fonts) | Themes auf Artifacts anwenden |
| `/doc-coauthoring` | Strukturierter Workflow fuer Dokumentation | Proposals, Specs, Docs schreiben |
| `/brand-guidelines` | Anthropic Brand-Farben & Typografie | Corporate Design anwenden |
| `/algorithmic-art` | Generative Kunst mit p5.js | Flow Fields, Partikel-Systeme |
| `/internal-comms` | Interne Kommunikation Templates | Newsletter, Status-Reports, FAQs |
| `/slack-gif-creator` | Animierte GIFs fuer Slack | GIFs erstellen |

### Skills installieren

1. Oeffne [claude.ai/customize/skills](https://claude.ai/customize/skills)
2. Klicke auf `+` > `Faehigkeiten durchsuchen`
3. Klicke auf `+` neben dem gewuenschten Skill

---

## Plugins (Claude Code)

Plugins sind umfangreichere Erweiterungen fuer Claude Code (CLI/Desktop).

### Offizielle Anthropic Plugins

| Plugin | Beschreibung | Installbefehl |
|---|---|---|
| `frontend-design` | Production-grade Frontend-Code mit distinctivem Design | `/plugin install frontend-design@claude-plugins-official` |
| `code-review` | Strukturierte Code Reviews | `/plugin install code-review@claude-plugins-official` |
| `code-simplifier` | Code vereinfachen und optimieren | `/plugin install code-simplifier@claude-plugins-official` |
| `feature-dev` | Feature-Entwicklung Workflow | `/plugin install feature-dev@claude-plugins-official` |
| `security-guidance` | Security Best Practices & Audits | `/plugin install security-guidance@claude-plugins-official` |
| `commit-commands` | Git Commit Workflows | `/plugin install commit-commands@claude-plugins-official` |
| `pr-review-toolkit` | PR Review Tools | `/plugin install pr-review-toolkit@claude-plugins-official` |
| `hookify` | Claude Code Hooks erstellen | `/plugin install hookify@claude-plugins-official` |
| `mcp-server-dev` | MCP Server entwickeln | `/plugin install mcp-server-dev@claude-plugins-official` |
| `claude-md-management` | CLAUDE.md Dateien verwalten | `/plugin install claude-md-management@claude-plugins-official` |
| `plugin-dev` | Eigene Plugins entwickeln | `/plugin install plugin-dev@claude-plugins-official` |
| `playground` | Experimentieren & Prototyping | `/plugin install playground@claude-plugins-official` |

### Community Plugins

| Plugin | Beschreibung | Installbefehl |
|---|---|---|
| `superpowers` | TDD, Brainstorming, Subagent Development, Code Review (355K+ Installs) | `/plugin install superpowers@claude-plugins-official` |
| `claude-mem` | Persistentes Memory-System mit SQLite, Vektor-Suche, Web-Viewer (45.9K Stars) | `npx claude-mem install` |

### Externe Integrationen (Plugin Marketplace)

| Plugin | Beschreibung |
|---|---|
| `github` | GitHub Integration |
| `gitlab` | GitLab Integration |
| `linear` | Linear Issue Tracker |
| `asana` | Asana Projektmanagement |
| `slack` | Slack Messaging |
| `discord` | Discord Bot |
| `telegram` | Telegram Bot |
| `supabase` | Supabase Backend |
| `firebase` | Firebase Backend |
| `playwright` | Browser-Testing |
| `terraform` | Infrastructure as Code |
| `context7` | Context Management |

---

## MCP-Server (Integrationen)

MCP-Server verbinden Claude Code mit externen Tools und APIs.

| MCP-Server | Beschreibung |
|---|---|
| **Figma** | Design-to-Code, Screenshots, Variablen, Code Connect |
| **Crypto.com Exchange** | Ticker, Candlesticks, Order Book, Trades |
| **Claude in Chrome** | Browser-Automatisierung, Screenshots, DOM-Interaktion |
| **Claude Preview** | Dev-Server starten, Screenshots, Accessibility-Tests |
| **Indeed** | Job-Suche, Firmendaten, Gehaltsinformationen |
| **Computer Use** | macOS Desktop-Automatisierung |

### MCP-Server konfigurieren

MCP-Server werden in `.mcp.json` im Projektverzeichnis oder global konfiguriert:

```json
{
  "mcpServers": {
    "mein-server": {
      "type": "stdio",
      "command": "npx",
      "args": ["mein-mcp-server"]
    }
  }
}
```

---

## gstack

[gstack](https://github.com/garrytan/gstack) von Garry Tan (Y Combinator CEO) - 23 opinionierte Tools die als virtuelles Engineering-Team fungieren. 65.8K Stars.

### Sprint-Workflow

```
Think > Plan > Build > Review > Test > Ship > Reflect
```

### Alle gstack Skills

#### Planung & Strategie

| Skill | Rolle | Beschreibung |
|---|---|---|
| `/office-hours` | YC Office Hours | 6 Forcing Questions, reframt das Produkt bevor Code geschrieben wird |
| `/plan-ceo-review` | CEO / Founder | 10-Star Product finden, 4 Modi: Expansion, Selective, Hold, Reduction |
| `/plan-eng-review` | Eng Manager | Architektur, Datenfluss, Diagramme, Edge Cases, Tests |
| `/plan-design-review` | Senior Designer | Jede Design-Dimension 0-10 bewerten, AI Slop Detection |
| `/plan-devex-review` | DX Lead | Developer Experience Review, TTHW Benchmarks, 20-45 Forcing Questions |
| `/autoplan` | Review Pipeline | CEO + Design + Eng Review automatisch hintereinander |

#### Design

| Skill | Rolle | Beschreibung |
|---|---|---|
| `/design-consultation` | Design Partner | Komplettes Design System von Grund auf erstellen |
| `/design-shotgun` | Design Explorer | 4-6 AI Mockup-Varianten generieren, Vergleichsboard oeffnen |
| `/design-html` | Design Engineer | Mockup in production-quality HTML/CSS umwandeln (30KB, zero deps) |
| `/design-review` | Designer Who Codes | Visual Audit + automatische Fixes mit Before/After Screenshots |

#### Code & Review

| Skill | Rolle | Beschreibung |
|---|---|---|
| `/review` | Staff Engineer | Pre-Landing PR Review, findet Bugs die CI nicht findet |
| `/investigate` | Debugger | Systematisches Root-Cause Debugging in 4 Phasen |
| `/codex` | Second Opinion | Unabhaengiges Code Review von OpenAI Codex CLI |

#### QA & Testing

| Skill | Rolle | Beschreibung |
|---|---|---|
| `/qa` | QA Lead | App testen, Bugs finden UND fixen, Regression Tests generieren |
| `/qa-only` | QA Reporter | Nur Bug-Report ohne Code-Aenderungen |
| `/browse` | Browser | Headless Browser fuer Navigation, Screenshots, Interaktion |
| `/benchmark` | Performance Engineer | Page Load, Core Web Vitals, Resource Sizes |
| `/canary` | SRE | Post-Deploy Monitoring fuer Errors und Performance |

#### Shipping & Deployment

| Skill | Rolle | Beschreibung |
|---|---|---|
| `/ship` | Release Engineer | Tests, Coverage, Push, PR erstellen |
| `/land-and-deploy` | Release Engineer | PR mergen, CI abwarten, Production Health verifizieren |
| `/document-release` | Technical Writer | Alle Projekt-Docs automatisch aktualisieren |

#### Security & Safety

| Skill | Rolle | Beschreibung |
|---|---|---|
| `/cso` | Chief Security Officer | OWASP Top 10 + STRIDE Threat Model |
| `/careful` | Safety | Warnung vor destruktiven Befehlen (rm -rf, DROP TABLE, force-push) |
| `/freeze` | Edit Lock | Datei-Edits auf ein Verzeichnis beschraenken |
| `/guard` | Full Safety | /careful + /freeze kombiniert |

#### Sonstiges

| Skill | Rolle | Beschreibung |
|---|---|---|
| `/retro` | Eng Manager | Woechentliche Retrospektive mit Team-Breakdowns |
| `/learn` | Memory | Projekt-spezifische Learnings verwalten |
| `/gstack-upgrade` | Self-Updater | gstack auf neueste Version updaten |
| `/pair-agent` | Multi-Agent | Browser mit anderem AI Agent teilen |

### gstack installieren

```bash
# In Claude Code eingeben:
git clone --single-branch --depth 1 https://github.com/garrytan/gstack.git ~/.claude/skills/gstack
cd ~/.claude/skills/gstack && ./setup
```

Voraussetzung: [Bun](https://bun.sh) muss installiert sein (`curl -fsSL https://bun.sh/install | bash`).

---

## Superpowers Plugin

[Superpowers](https://github.com/obra/superpowers) von Jesse Vincent - Skills-Framework fuer strukturierte Software-Entwicklung. 138K Stars.

### Skills

| Skill | Beschreibung |
|---|---|
| `brainstorming` | Socratic Design-Verfeinerung vor dem Coden |
| `writing-plans` | Detaillierte Implementierungsplaene erstellen |
| `executing-plans` | Batch Execution mit Checkpoints |
| `subagent-driven-development` | Subagenten mit Two-Stage Review |
| `test-driven-development` | RED-GREEN-REFACTOR Zyklus |
| `systematic-debugging` | 4-Phasen Root Cause Analyse |
| `using-git-worktrees` | Parallele Entwicklung auf separaten Branches |
| `requesting-code-review` | Pre-Review Checkliste |
| `receiving-code-review` | Auf Code Review Feedback reagieren |
| `verification-before-completion` | Verifizieren bevor "fertig" gemeldet wird |
| `finishing-a-development-branch` | Branch abschliessen (Merge/PR/Keep/Discard) |

### Superpowers installieren

```bash
# In Claude Code eingeben:
/plugin install superpowers@claude-plugins-official
```

---

## claude-mem

[claude-mem](https://github.com/thedotmack/claude-mem) - Persistentes Memory-System das automatisch alles erfasst. 45.9K Stars.

### Features

- Automatisches Erfassen aller Tool-Nutzungen
- Semantische Suche in Projekt-Historie (`/mem-search`)
- Web-Viewer UI auf `http://localhost:37777`
- Kontext-Injection in neue Sessions
- Progressive Disclosure fuer Token-Effizienz

### claude-mem installieren

```bash
npx claude-mem install
```

### claude-mem nutzen

| Befehl | Beschreibung |
|---|---|
| `/mem-search` | Vergangene Sessions durchsuchen |
| `/smart-explore` | Token-optimierte Code-Exploration |
| `/make-plan` | Implementierungsplan erstellen |
| `/do` | Plan mit Subagenten ausfuehren |
| `/timeline-report` | Projekt-History als Narrativ |

---

## Installation - Komplettsetup

### 1. Bun installieren (Voraussetzung fuer gstack)

```bash
curl -fsSL https://bun.sh/install | bash
```

### 2. gstack installieren

```bash
git clone --single-branch --depth 1 https://github.com/garrytan/gstack.git ~/.claude/skills/gstack
cd ~/.claude/skills/gstack && ./setup
```

### 3. claude-mem installieren

```bash
npx claude-mem install
```

### 4. Plugins in Claude Code aktivieren

```
/plugin install superpowers@claude-plugins-official
/plugin install frontend-design@claude-plugins-official
```

### 5. Skills in claude.ai installieren

Oeffne [claude.ai/customize/skills](https://claude.ai/customize/skills) und installiere alle Anthropic Skills.

### 6. Claude Code neustarten

```
/exit
claude
```

---

## Nutzungsbeispiele

### Feature von Grund auf bauen

```
/office-hours          # Idee verfeinern
/plan-ceo-review       # CEO-Perspektive
/plan-eng-review       # Architektur festlegen
/autoplan              # Automatischer Review-Durchlauf
# Code schreiben...
/review                # Code Review
/qa https://localhost   # QA Testing
/ship                  # PR erstellen
```

### Bug fixen

```
/investigate           # Root Cause finden
# Fix implementieren...
/review                # Fix reviewen
/ship                  # Shippen
```

### Design erstellen

```
/design-consultation   # Design System erstellen
/design-shotgun        # Varianten generieren
/design-html           # In Production HTML umwandeln
```

### Security Audit

```
/cso                   # OWASP Top 10 + STRIDE
```

### Wochenrueckblick

```
/retro                 # Engineering Retrospektive
```

---

## Lizenz

Dieses Setup-Guide ist frei verfuegbar. Die einzelnen Tools haben eigene Lizenzen:
- gstack: MIT
- Superpowers: MIT
- claude-mem: AGPL-3.0
- Anthropic Skills: Siehe jeweilige LICENSE.txt
