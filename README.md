# Claude Code Setup Guide

Mein komplettes Claude Code Setup: Skills, Plugins, MCP-Server und Tools.

## Inhaltsverzeichnis

- [Skills (claude.ai)](#skills-claudeai)
- [Plugins (Claude Code)](#plugins-claude-code)
- [MCP-Server (Integrationen)](#mcp-server-integrationen)
- [gstack (Garry Tan's Engineering Stack)](#gstack)
- [GitNexus (Code Knowledge Graph)](#gitnexus)
- [ECC (Everything Claude Code)](#ecc-everything-claude-code)
- [Installation](#installation)
- [Nutzungsbeispiele](#nutzungsbeispiele)
- [Claude Code Terminal – Shortcuts & Befehle](#claude-code-terminal--shortcuts--befehle)

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
| **GitNexus** | Code Knowledge Graph, Impact-Analyse, Refactoring, PR-Review |

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

## GitNexus

[GitNexus](https://www.npmjs.com/package/gitnexus) - Code Knowledge Graph der dein Repository als Graph indexiert und als MCP-Server bereitstellt. Analysiert Abhaengigkeiten, Impact und Ausfuehrungsfluesse.

### Features

- Automatische Graph-Analyse: Nodes (Dateien, Funktionen, Methoden), Edges (Abhaengigkeiten), Clusters (Communities)
- Impact-Analyse: Was bricht, wenn du etwas aenderst?
- Kontext-Suche: 360-Grad-Ansicht von Code-Symbolen (Caller, Callees, Prozesse)
- MCP-Server: Tools direkt in Claude Code und Cursor verfuegbar
- Skills: 7 Skills fuer Debugging, Refactoring, PR-Review, Impact-Analyse, Exploration

### GitNexus Skills

| Skill | Beschreibung |
|---|---|
| `/gitnexus-guide` | Verfuegbare Tools und Workflow-Referenz |
| `/gitnexus-exploring` | Architektur verstehen, Ausfuehrungsfluesse verfolgen |
| `/gitnexus-debugging` | Bugs tracen, Fehlerquellen finden |
| `/gitnexus-refactoring` | Sicheres Umbenennen, Extrahieren, Verschieben |
| `/gitnexus-impact-analysis` | Blast-Radius vor Aenderungen pruefen |
| `/gitnexus-pr-review` | PR reviewen mit Graph-Kontext |
| `/gitnexus-cli` | CLI-Befehle (analyze, status, wiki, query) |

### GitNexus CLI

| Befehl | Beschreibung |
|---|---|
| `npx gitnexus analyze` | Repository indexieren |
| `npx gitnexus setup` | MCP fuer Claude Code / Cursor einrichten |
| `npx gitnexus status` | Index-Status pruefen |
| `npx gitnexus query "<suche>"` | Freitext-Suche im Knowledge Graph |
| `npx gitnexus context <symbol>` | 360-Grad-Ansicht eines Symbols |
| `npx gitnexus impact <target>` | Blast-Radius-Analyse |
| `npx gitnexus wiki` | Repository-Wiki generieren (braucht API Key) |
| `npx gitnexus list` | Alle indexierten Repos anzeigen |

### GitNexus installieren

```bash
# 1. Repository analysieren
cd dein-projekt
npx gitnexus analyze

# 2. MCP-Server einrichten (Claude Code + Cursor)
npx gitnexus setup
```

---

## ECC (Everything Claude Code)

[Everything Claude Code](https://github.com/affaan-m/everything-claude-code) (ECC) von Affaan - Universelles Rules-, Agents- und Skills-Framework fuer Claude Code. Liefert sprachspezifische Coding-Rules, Quality-Workflows und spezialisierte Skills. v2.0.0-rc.1.

### Profile

| Profil | Inhalt |
|---|---|
| `minimal` | Rules, Agents, Commands, Platform-Configs, Workflow-Quality (ohne Hooks Runtime) |
| `full` | Alles inkl. Hooks Runtime fuer globale Enforcement |

### Rules (sprachspezifisch)

ECC installiert opinionierte Coding-Rules fuer jede Sprache unter `~/.claude/rules/ecc/`:

| Kategorie | Beschreibung |
|---|---|
| `common/` | Agents, Code Review, Coding Style, Development Workflow, Git, Hooks, Patterns, Performance, Security, Testing |
| `typescript/` | TypeScript-spezifische Rules |
| `python/` | Python-spezifische Rules |
| `rust/` | Rust-spezifische Rules |
| `golang/` | Go-spezifische Rules |
| `kotlin/` | Kotlin-spezifische Rules |
| `java/` | Java-spezifische Rules |
| `cpp/` | C++-spezifische Rules |
| `swift/` | Swift-spezifische Rules |
| `dart/` | Dart/Flutter-spezifische Rules |
| `csharp/` | C#-spezifische Rules |
| `php/` | PHP-spezifische Rules |
| `perl/` | Perl-spezifische Rules |
| `web/` | Web/Frontend-spezifische Rules |

### ECC Skills

Skills werden unter `~/.claude/skills/ecc/` installiert:

| Skill | Beschreibung |
|---|---|
| `council` | Multi-Perspektiven Code Review mit virtuellen Experten |
| `tdd-workflow` | Test-Driven Development Workflow |
| `verification-loop` | Automatische Verifikations-Schleifen |
| `e2e-testing` | End-to-End Testing Workflow |
| `eval-harness` | Deterministische Repository-Audits mit Scorecard |
| `code-tour` | Codebase-Touren erstellen und navigieren |
| `continuous-learning` | Patterns aus Sessions extrahieren und speichern |
| `continuous-learning-v2` | Erweiterte Version mit Observer-Agents |
| `strategic-compact` | Intelligentes Context-Compacting |
| `plankton-code-quality` | Code-Quality Pipeline |
| `skill-stocktake` | Skill-Portfolio analysieren |
| `hookify-rules` | Rules in Hooks umwandeln |
| `iterative-retrieval` | Iterative Code-Retrieval |
| `agent-introspection-debugging` | Agent-Verhalten debuggen |
| `agent-sort` | Agents priorisieren und sortieren |
| `ai-regression-testing` | AI-spezifische Regressionstests |
| `configure-ecc` | ECC-Konfiguration anpassen |

### ECC Commands

| Command | Beschreibung |
|---|---|
| `/plan` | Anforderungen pruefen, Risiken bewerten, Implementierungsplan erstellen |
| `/build-fix` | Build-System erkennen und Fehler inkrementell fixen |
| `/code-review` | Code Review (lokal oder GitHub PR) |
| `/test-coverage` | Coverage analysieren, Luecken finden, Tests generieren |
| `/review-pr` | Umfassendes PR Review mit spezialisierten Agents |
| `/checkpoint` | Workflow-Checkpoints erstellen und verifizieren |
| `/update-docs` | Dokumentation aus Source-of-Truth synchronisieren |
| `/update-codemaps` | Architektur-Codemaps generieren |
| `/refactor-clean` | Dead Code sicher identifizieren und entfernen |
| `/harness-audit` | Repository-Audit mit priorisierter Scorecard |
| `/quality-gate` | ECC Quality Pipeline ausfuehren |
| `/santa-loop` | Dual-Review Convergence Loop (zwei Reviewer muessen zustimmen) |
| `/model-route` | Bestes Model-Tier fuer aktuelle Aufgabe empfehlen |
| Sprachspezifisch | `/rust-review`, `/rust-build`, `/rust-test`, `/go-review`, `/go-build`, `/go-test`, `/kotlin-review`, `/kotlin-build`, `/kotlin-test`, `/cpp-review`, `/cpp-build`, `/cpp-test`, `/python-review`, `/flutter-review`, `/flutter-build`, `/flutter-test` |

### ECC installieren

```bash
# Repository klonen
git clone https://github.com/affaan-m/everything-claude-code.git /tmp/everything-claude-code

# Minimal-Profil installieren (ohne Hooks Runtime)
cd /tmp/everything-claude-code && ./install.sh --profile minimal --target claude

# Oder: Volles Profil mit Hooks
cd /tmp/everything-claude-code && ./install.sh --target claude
```

> **Wichtig:** Nicht mit dem Claude Code Plugin (`/plugin install`) kombinieren – waehle einen Installationspfad.

### ECC deinstallieren

```bash
cd /tmp/everything-claude-code && ./install.sh --reset --target claude
```

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

### 5. ECC installieren

```bash
git clone https://github.com/affaan-m/everything-claude-code.git /tmp/everything-claude-code
cd /tmp/everything-claude-code && ./install.sh --profile minimal --target claude
```

### 6. GitNexus einrichten

```bash
cd dein-projekt
npx gitnexus analyze
npx gitnexus setup
```

### 7. Skills in claude.ai installieren

Oeffne [claude.ai/customize/skills](https://claude.ai/customize/skills) und installiere alle Anthropic Skills.

### 8. Claude Code neustarten

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

## Claude Code Terminal – Shortcuts & Befehle

### Optimale Nutzung

Claude Code ist kein klassischer Chat – es ist ein terminalnativer AI-Pair-Programmer, der direkt in deinem Projekt arbeitet. Der Schlüssel zur produktiven Nutzung liegt in drei Gewohnheiten:

1. **Starte jedes neue Repo mit `/init`** – damit wird eine `CLAUDE.md` erstellt, die Claude dauerhaft Kontext über dein Projekt gibt. Das spart dir bei jeder Session Erklärungsaufwand.
2. **Nutze Plan Mode (`Shift+Tab`) vor jeder grösseren Änderung** – so bekommst du erst eine Analyse, bevor Code verändert wird. Das verhindert, dass Claude in die falsche Richtung läuft.
3. **Arbeite in kleinen, klaren Aufgaben** – statt „baue mir die ganze App" lieber einzelne Features oder Fixes beauftragen. Claude Code liefert deutlich bessere Ergebnisse, wenn der Scope klar ist.

Weitere Tipps: Nutze `/compact` regelmässig bei langen Sessions, um Token zu sparen. Verwende `Ctrl+S` zum Stashen von Prompts, wenn du zwischendurch etwas anderes fragen willst. Und verbinde deine IDE mit `/ide`, damit Diffs und File-Reviews in VS Code statt im Terminal landen.

---

### Keyboard Shortcuts (im REPL)

| Kürzel | Funktion |
|---|---|
| `Escape` | Generation abbrechen |
| `Escape Escape` | Letzten Prompt bearbeiten / Conversation zurückspulen |
| `Ctrl+C` | Abbrechen (2x = Hard Exit) |
| `Ctrl+D` | Session beenden |
| `Ctrl+L` | Screen clearen (History bleibt) |
| `Ctrl+S` | Prompt stashen (zwischenparken) |
| `Ctrl+R` | History durchsuchen |
| `Ctrl+G` | Prompt im externen Editor öffnen |
| `Ctrl+B` | Bash-Befehl in Background verschieben |
| `Ctrl+O` | Transcript Viewer öffnen |
| `Shift+Tab` | Permission-Modus wechseln (Normal → Auto → Plan) |
| `\ + Enter` | Mehrzeilige Eingabe (überall) |
| `↑ / ↓` | Command History navigieren |

### Slash Commands

| Befehl | Funktion |
|---|---|
| `/init` | CLAUDE.md für das Repo erstellen |
| `/compact` | Kontext komprimieren (Token sparen) |
| `/clear` | Chat-History löschen, frisch starten |
| `/review` | Code-Review (Bugs, Style, Performance) |
| `/cost` | Bisherige Token-Kosten anzeigen |
| `/context` | Context-Breakdown anzeigen |
| `/model` | Model wechseln (Sonnet/Opus) |
| `/ide` | VS Code / JetBrains anbinden |
| `/resume` | Frühere Session wiederaufnehmen |
| `/terminal-setup` | Shift+Enter für Newlines einrichten |
| `/add-dir <path>` | Zusätzliche Verzeichnisse einbinden |
| `/mcp` | MCP Server verwalten |
| `/btw` | Side-Question (kein Tool-Zugriff, nutzt nur bestehenden Kontext) |

### CLI Flags

| Flag | Funktion |
|---|---|
| `claude -c` | Letzte Session fortsetzen |
| `claude -r <id>` | Bestimmte Session resumieren |
| `claude -p "query"` | One-Shot ohne REPL |
| `claude --max-turns 5` | Agent-Loops begrenzen |
| `claude --output-format json` | JSON-Output für Automation |
| `cat file \| claude -p "..."` | Piped Input verarbeiten |
| `claude --allowedTools "Read" "Write"` | Tool-Permissions setzen |
| `claude --add-dir ../other` | Weitere Verzeichnisse einbinden |

---

Dieses Setup-Guide ist frei verfuegbar. Die einzelnen Tools haben eigene Lizenzen:
- gstack: MIT
- Superpowers: MIT
- claude-mem: AGPL-3.0
- GitNexus: MIT
- ECC: MIT
- Anthropic Skills: Siehe jeweilige LICENSE.txt
