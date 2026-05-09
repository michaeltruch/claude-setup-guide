# Claude Code Setup Guide

Mein komplettes Claude Code Setup: Skills, Plugins, MCP-Server und Tools.

## Inhaltsverzeichnis

- [Claude Code – Plattformen & Installation](#claude-code--plattformen--installation)
- [Skills (claude.ai)](#skills-claudeai)
- [Plugins (Claude Code)](#plugins-claude-code)
- [MCP-Server (Integrationen)](#mcp-server-integrationen)
- [gstack (Garry Tan's Engineering Stack)](#gstack)
- [Superpowers Plugin](#superpowers-plugin)
- [claude-mem](#claude-mem)
- [GitNexus (Code Knowledge Graph)](#gitnexus)
- [ECC (Everything Claude Code)](#ecc-everything-claude-code)
- [Installation - Komplettsetup](#installation---komplettsetup)
- [Nutzungsbeispiele](#nutzungsbeispiele)
- [Claude Code Terminal – Shortcuts & Befehle](#claude-code-terminal--shortcuts--befehle)

---

## Claude Code – Plattformen & Installation

Claude Code ist ein agentischer AI-Coding-Assistent, der im Terminal, in IDEs, als Desktop-App und im Browser laeuft.

### Installationsmethoden

| Methode | Befehl | Hinweis |
|---|---|---|
| **Native Install (empfohlen)** | `curl -fsSL https://claude.ai/install.sh \| bash` | macOS, Linux, WSL – Auto-Updates |
| **Homebrew** | `brew install --cask claude-code` | macOS – kein Auto-Update, `brew upgrade` noetig |
| **WinGet** | `winget install Anthropic.ClaudeCode` | Windows – kein Auto-Update |
| **Windows PowerShell** | `irm https://claude.ai/install.ps1 \| iex` | Windows nativ |
| **NPM (veraltet)** | `npm install -g @anthropic-ai/claude-code` | Wird nicht mehr empfohlen |

### Plattformen

| Plattform | Beschreibung | Setup |
|---|---|---|
| **Terminal (CLI)** | Voller Funktionsumfang, Dateien bearbeiten, Befehle ausfuehren | `claude` im Projektverzeichnis |
| **VS Code / Cursor** | Inline Diffs, @-Mentions, Plan Review, Conversation History | Extension "Claude Code" installieren |
| **JetBrains** | IntelliJ, PyCharm, WebStorm – interaktive Diffs | Plugin aus JetBrains Marketplace |
| **Desktop App** | Standalone, visuelle Diffs, mehrere Sessions parallel, Scheduled Tasks | Download von [claude.ai](https://claude.ai) |
| **Web** | Kein lokales Setup noetig, lange Tasks starten und spaeter pruefen | [claude.ai/code](https://claude.ai/code) |
| **Chrome** | Live Web-Apps debuggen | `claude --chrome` |
| **iOS App** | Tasks von unterwegs starten | Claude App im App Store |

### Voraussetzungen

- Node.js 18+
- Git (empfohlen)
- Claude Subscription oder Anthropic Console Account

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
| **Google Drive** | Dateien lesen, erstellen, durchsuchen |

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
| `dispatching-parallel-agents` | Parallele Subagenten fuer unabhaengige Tasks |
| `writing-skills` | Neue Skills erstellen und verifizieren |

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

### 1. Claude Code installieren

```bash
# macOS / Linux (empfohlen)
curl -fsSL https://claude.ai/install.sh | bash

# Oder via Homebrew
brew install --cask claude-code

# Windows
winget install Anthropic.ClaudeCode
```

### 2. Bun installieren (Voraussetzung fuer gstack)

```bash
curl -fsSL https://bun.sh/install | bash
```

### 3. gstack installieren

```bash
git clone --single-branch --depth 1 https://github.com/garrytan/gstack.git ~/.claude/skills/gstack
cd ~/.claude/skills/gstack && ./setup
```

### 4. claude-mem installieren

```bash
npx claude-mem install
```

### 5. Plugins in Claude Code aktivieren

```
/plugin install superpowers@claude-plugins-official
/plugin install frontend-design@claude-plugins-official
```

### 6. ECC installieren

```bash
git clone https://github.com/affaan-m/everything-claude-code.git /tmp/everything-claude-code
cd /tmp/everything-claude-code && ./install.sh --profile minimal --target claude
```

### 7. GitNexus einrichten

```bash
cd dein-projekt
npx gitnexus analyze
npx gitnexus setup
```

### 8. Skills in claude.ai installieren

Oeffne [claude.ai/customize/skills](https://claude.ai/customize/skills) und installiere alle Anthropic Skills.

### 9. Claude Code neustarten

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

## Claude Code Terminal – Shortcuts & Befehle

### Optimale Nutzung

Claude Code ist kein klassischer Chat – es ist ein terminalnativer AI-Pair-Programmer, der direkt in deinem Projekt arbeitet. Der Schluessel zur produktiven Nutzung liegt in drei Gewohnheiten:

1. **Starte jedes neue Repo mit `/init`** – damit wird eine `CLAUDE.md` erstellt, die Claude dauerhaft Kontext ueber dein Projekt gibt. Das spart dir bei jeder Session Erklaerungsaufwand.
2. **Nutze Plan Mode (`Shift+Tab`) vor jeder groesseren Aenderung** – so bekommst du erst eine Analyse, bevor Code veraendert wird. Das verhindert, dass Claude in die falsche Richtung laeuft.
3. **Arbeite in kleinen, klaren Aufgaben** – statt "baue mir die ganze App" lieber einzelne Features oder Fixes beauftragen. Claude Code liefert deutlich bessere Ergebnisse, wenn der Scope klar ist.

Weitere Tipps: Nutze `/compact` regelmaessig bei langen Sessions, um Token zu sparen. Verwende `Ctrl+S` zum Stashen von Prompts, wenn du zwischendurch etwas anderes fragen willst. Und verbinde deine IDE mit `/ide`, damit Diffs und File-Reviews in VS Code statt im Terminal landen.

---

### Keyboard Shortcuts – Allgemein

| Kuerzel | Funktion | Kontext |
|---|---|---|
| `Ctrl+C` | Abbrechen (2x = Hard Exit) | Standard Interrupt |
| `Ctrl+D` | Session beenden | EOF Signal |
| `Ctrl+L` | Screen neu zeichnen (History bleibt) | Terminal Redraw |
| `Ctrl+G` / `Ctrl+X Ctrl+E` | Prompt im externen Editor oeffnen | Default `$EDITOR` |
| `Ctrl+O` | Transcript Viewer ein/aus | Tool-Usage und MCP-Calls anzeigen |
| `Ctrl+R` | History durchsuchen (Reverse Search) | `Ctrl+S` wechselt Scope (Session/Projekt/Alle) |
| `Ctrl+B` | Bash-Befehl in Background | Tmux-User: 2x druecken |
| `Ctrl+T` | Task-Liste ein/aus | Zeigt bis zu 5 Tasks im Statusbereich |
| `Ctrl+S` | Prompt stashen (zwischenparken) | Prompt sichern und spaeter weiterarbeiten |
| `Ctrl+V` / `Cmd+V` | Bild aus Clipboard einfuegen | Fuegt `[Image #N]` Chip ein |
| `Ctrl+X Ctrl+K` | Alle Background-Agents beenden | 2x innerhalb 3 Sekunden zur Bestaetigung |
| `Shift+Tab` / `Alt+M` | Permission-Modus wechseln | default → acceptEdits → plan → auto → bypassPermissions |
| `Alt+P` / `Option+P` | Model wechseln | Sonnet ↔ Opus ohne Prompt zu loeschen |
| `Alt+T` / `Option+T` | Extended Thinking ein/aus | Tieferes Reasoning aktivieren |
| `Alt+O` / `Option+O` | Fast Mode ein/aus | Schnellerer Output |
| `Esc Esc` | Rewind / Zusammenfassen | Code und Conversation zurueckspulen |
| `↑ / ↓` | Command History navigieren | Am Rand des Inputs |

> **macOS:** Option/Alt-Shortcuts erfordern "Use Option as Meta Key" im Terminal (iTerm2: Settings → Profiles → Keys → General → "Esc+").

### Keyboard Shortcuts – Text-Editing

| Kuerzel | Funktion |
|---|---|
| `Ctrl+A` | Cursor zum Zeilenanfang |
| `Ctrl+E` | Cursor zum Zeilenende |
| `Ctrl+K` | Bis Zeilenende loeschen |
| `Ctrl+U` | Bis Zeilenanfang loeschen |
| `Ctrl+W` | Vorheriges Wort loeschen |
| `Ctrl+Y` | Geloeschten Text einfuegen (Paste) |
| `Alt+Y` | Nach `Ctrl+Y`: durch Paste-History wechseln |
| `Alt+B` | Cursor ein Wort zurueck |
| `Alt+F` | Cursor ein Wort vor |

### Mehrzeilige Eingabe

| Methode | Shortcut | Kontext |
|---|---|---|
| Quick Escape | `\` + `Enter` | Funktioniert in allen Terminals |
| Option Key | `Option+Enter` | macOS mit Meta-Key Konfiguration |
| Shift+Enter | `Shift+Enter` | Nativ in iTerm2, WezTerm, Ghostty, Kitty, Warp, Windows Terminal |
| Control | `Ctrl+J` | Funktioniert in jedem Terminal ohne Konfiguration |
| Paste Mode | Direkt einfuegen | Fuer Code-Bloecke, Logs |

### Quick Input Prefixes

| Prefix | Funktion | Beschreibung |
|---|---|---|
| `/` | Command / Skill | Slash Commands und Skills ausfuehren |
| `!` | Shell Mode | Befehle direkt ausfuehren, Output wird zum Kontext hinzugefuegt |
| `@` | File Mention | Datei-Pfad Autocomplete triggern |

---

### Slash Commands (Built-in)

| Befehl | Funktion |
|---|---|
| `/init` | CLAUDE.md fuer das Repo erstellen |
| `/compact` | Kontext komprimieren (Token sparen) |
| `/clear` | Chat-History loeschen, frisch starten |
| `/review` | Code-Review (Bugs, Style, Performance) |
| `/cost` | Bisherige Token-Kosten anzeigen |
| `/context` | Context-Breakdown anzeigen |
| `/model` | Model wechseln (Sonnet/Opus) |
| `/fast` | Fast Mode ein/aus (schnellerer Output) |
| `/ide` | VS Code / JetBrains anbinden |
| `/resume` | Fruehere Session wiederaufnehmen |
| `/rename` | Session umbenennen (erscheint in `/resume` und Prompt Bar) |
| `/terminal-setup` | Shift+Enter fuer Newlines einrichten (VS Code, Cursor, Alacritty, Zed) |
| `/add-dir <path>` | Zusaetzliche Verzeichnisse einbinden |
| `/mcp` | MCP Server verwalten |
| `/config` | Claude Code Einstellungen oeffnen (Editor Mode, Preferences) |
| `/theme` | Syntax-Highlighting und Farbschema waehlen |
| `/btw` | Side-Question (kein Tool-Zugriff, nutzt nur bestehenden Kontext, auch waehrend Claude arbeitet) |
| `/bug` | Bug direkt in Claude Code melden |
| `/recap` | Session-Zusammenfassung manuell generieren |
| `/schedule` | Wiederkehrende Tasks als Routines einrichten |
| `/desktop` | Session an Desktop App uebergeben (fuer visuelle Diff-Review) |
| `/voice` | Voice Dictation konfigurieren (`/voice tap` fuer Tap-to-Toggle) |
| `/plugin` | Plugins verwalten (install, list, remove) |
| `/ultrareview` | Umfassendes Code Review |

---

### CLI Commands

| Befehl | Beschreibung | Beispiel |
|---|---|---|
| `claude` | Interaktive Session starten | `claude` |
| `claude "query"` | Session mit initialem Prompt | `claude "explain this project"` |
| `claude -p "query"` | One-Shot ohne REPL (Print Mode) | `claude -p "explain this function"` |
| `cat file \| claude -p "..."` | Piped Input verarbeiten | `cat logs.txt \| claude -p "explain"` |
| `claude -c` | Letzte Session fortsetzen | `claude -c` |
| `claude -c -p "query"` | Letzte Session fortsetzen (SDK) | `claude -c -p "Check for type errors"` |
| `claude -r "<session>"` | Session per ID oder Name resumieren | `claude -r "auth-refactor"` |
| `claude update` | Auf neueste Version updaten | `claude update` |
| `claude install [version]` | Spezifische Version installieren | `claude install stable` |
| `claude auth login` | Anmelden (`--sso` fuer SSO, `--console` fuer API) | `claude auth login --console` |
| `claude auth logout` | Abmelden | `claude auth logout` |
| `claude auth status` | Auth-Status als JSON (`--text` fuer lesbare Ausgabe) | `claude auth status` |
| `claude agents` | Alle konfigurierten Subagents auflisten | `claude agents` |
| `claude auto-mode defaults` | Auto-Mode Classifier Rules als JSON | `claude auto-mode defaults` |
| `claude mcp` | MCP Server konfigurieren | `claude mcp` |
| `claude plugin` | Plugins verwalten | `claude plugin install ...` |
| `claude project purge` | Lokalen State fuer Projekt loeschen | `claude project purge ~/repo --dry-run` |
| `claude remote-control` | Remote Control Server starten | `claude remote-control --name "My Project"` |
| `claude setup-token` | Long-lived OAuth Token fuer CI generieren | `claude setup-token` |
| `claude ultrareview` | Ultrareview non-interaktiv ausfuehren | `claude ultrareview 1234 --json` |

### CLI Flags

#### Session & Modus

| Flag | Funktion | Beispiel |
|---|---|---|
| `--continue`, `-c` | Letzte Session im Verzeichnis fortsetzen | `claude -c` |
| `--resume`, `-r` | Session per ID/Name resumieren | `claude -r auth-refactor` |
| `--print`, `-p` | Print Mode (non-interactive) | `claude -p "query"` |
| `--name`, `-n` | Session benennen | `claude -n "my-feature"` |
| `--fork-session` | Beim Resume neue Session-ID erstellen | `claude -r abc --fork-session` |
| `--from-pr` | Sessions zu einem PR resumieren | `claude --from-pr 123` |
| `--session-id` | Spezifische Session-ID (UUID) | `claude --session-id "550e..."` |

#### Permission & Sicherheit

| Flag | Funktion | Beispiel |
|---|---|---|
| `--permission-mode` | Permission-Modus setzen (`default`, `acceptEdits`, `plan`, `auto`, `bypassPermissions`) | `claude --permission-mode plan` |
| `--dangerously-skip-permissions` | Alle Permission-Prompts ueberspringen | `claude --dangerously-skip-permissions` |
| `--allow-dangerously-skip-permissions` | `bypassPermissions` zum Shift+Tab Cycle hinzufuegen | `claude --permission-mode plan --allow-dangerously-skip-permissions` |
| `--allowedTools` | Tools ohne Permission-Prompt erlauben | `claude --allowedTools "Bash(git *)" "Read"` |
| `--disallowedTools` | Tools komplett deaktivieren | `claude --disallowedTools "Edit"` |
| `--tools` | Verfuegbare Tools einschraenken | `claude --tools "Bash,Edit,Read"` |

#### Model & Output

| Flag | Funktion | Beispiel |
|---|---|---|
| `--model` | Model setzen (Alias oder vollstaendiger Name) | `claude --model sonnet` |
| `--effort` | Effort Level (`low`, `medium`, `high`, `xhigh`, `max`) | `claude --effort high` |
| `--fallback-model` | Fallback bei Ueberlastung (Print Mode) | `claude -p --fallback-model sonnet "query"` |
| `--output-format` | Output-Format (`text`, `json`, `stream-json`) | `claude -p --output-format json "query"` |
| `--input-format` | Input-Format (`text`, `stream-json`) | `claude -p --input-format stream-json` |
| `--json-schema` | Validierter JSON-Output nach Schema (Print Mode) | `claude -p --json-schema '{...}' "query"` |
| `--verbose` | Ausfuehrliches Turn-by-Turn Logging | `claude --verbose` |
| `--version`, `-v` | Versionsnummer anzeigen | `claude -v` |

#### System Prompt

| Flag | Funktion | Beispiel |
|---|---|---|
| `--system-prompt` | Gesamten System-Prompt ersetzen | `claude --system-prompt "You are a Python expert"` |
| `--system-prompt-file` | System-Prompt aus Datei laden | `claude --system-prompt-file ./prompt.txt` |
| `--append-system-prompt` | Text an System-Prompt anhaengen | `claude --append-system-prompt "Always use TS"` |
| `--append-system-prompt-file` | Datei-Inhalt an System-Prompt anhaengen | `claude --append-system-prompt-file ./rules.txt` |

#### Verzeichnisse & Worktrees

| Flag | Funktion | Beispiel |
|---|---|---|
| `--add-dir` | Zusaetzliche Arbeitsverzeichnisse | `claude --add-dir ../apps ../lib` |
| `--worktree`, `-w` | Isolierten Git Worktree starten | `claude -w feature-auth` |
| `--tmux` | Tmux-Session fuer Worktree erstellen | `claude -w feature-auth --tmux` |

#### Agents & MCP

| Flag | Funktion | Beispiel |
|---|---|---|
| `--agent` | Agent fuer Session setzen | `claude --agent my-custom-agent` |
| `--agents` | Subagents dynamisch per JSON definieren | `claude --agents '{"reviewer":{...}}'` |
| `--mcp-config` | MCP-Server aus JSON-Datei laden | `claude --mcp-config ./mcp.json` |
| `--strict-mcp-config` | Nur MCP-Server aus `--mcp-config` nutzen | `claude --strict-mcp-config --mcp-config ./mcp.json` |
| `--plugin-dir` | Plugin aus Verzeichnis/ZIP laden | `claude --plugin-dir ./my-plugin` |
| `--plugin-url` | Plugin von URL laden | `claude --plugin-url https://...` |
| `--teammate-mode` | Agent-Team Display (`auto`, `in-process`, `tmux`) | `claude --teammate-mode tmux` |

#### Remote & Web

| Flag | Funktion | Beispiel |
|---|---|---|
| `--remote` | Neue Web-Session auf claude.ai erstellen | `claude --remote "Fix the login bug"` |
| `--remote-control`, `--rc` | Remote Control aktivieren | `claude --rc "My Project"` |
| `--teleport` | Web-Session ins lokale Terminal holen | `claude --teleport` |
| `--chrome` | Chrome Browser Integration aktivieren | `claude --chrome` |
| `--no-chrome` | Chrome Integration deaktivieren | `claude --no-chrome` |

#### Performance & Debugging

| Flag | Funktion | Beispiel |
|---|---|---|
| `--bare` | Minimal-Modus (keine Hooks, Skills, Plugins, MCP) | `claude --bare -p "query"` |
| `--debug` | Debug-Modus mit Kategorie-Filter | `claude --debug "api,mcp"` |
| `--debug-file` | Debug-Logs in Datei schreiben | `claude --debug-file /tmp/debug.log` |
| `--max-turns` | Agentic Turns begrenzen (Print Mode) | `claude -p --max-turns 3 "query"` |
| `--max-budget-usd` | API-Budget begrenzen (Print Mode) | `claude -p --max-budget-usd 5.00 "query"` |
| `--disable-slash-commands` | Alle Skills und Commands deaktivieren | `claude --disable-slash-commands` |
| `--no-session-persistence` | Sessions nicht speichern (Print Mode) | `claude -p --no-session-persistence "query"` |

---

### Features

#### CLAUDE.md – Persistente Projekt-Instruktionen

`CLAUDE.md` ist eine Markdown-Datei im Projekt-Root, die Claude bei jeder Session liest. Nutze sie fuer:

- Coding Standards und Konventionen
- Architektur-Entscheidungen
- Bevorzugte Libraries und Frameworks
- Review-Checklisten
- Build- und Test-Befehle

Claude baut zusaetzlich **Auto Memory** auf – Learnings wie Build-Commands und Debugging-Insights werden automatisch session-uebergreifend gespeichert.

#### Shell Mode (`!`)

Befehle direkt ausfuehren ohne Claude zu fragen:

```
! npm test
! git status
! ls -la
```

Output wird zum Konversations-Kontext hinzugefuegt. Unterstuetzt `Ctrl+B` fuer Background.

#### Voice Input

Spracheingabe aktivieren ueber `/voice`. `Space` halten zum Aufnehmen, oder `/voice tap` fuer Tap-to-Toggle.

#### Remote Control

Sessions von claude.ai oder der Claude App steuern:

```bash
claude --remote-control --name "My Project"
```

Ermoeglicht Arbeiten vom Handy oder einem anderen Geraet.

#### Routines (Scheduled Tasks)

Wiederkehrende Tasks automatisieren:

- **Routines** (`/schedule`): Laufen auf Anthropic-Infrastruktur, auch wenn dein Rechner aus ist
- **Desktop Scheduled Tasks**: Laufen lokal mit Zugriff auf deine Dateien
- **`/loop`**: Prompt innerhalb einer Session wiederholen

#### Agent Teams & Subagents

Mehrere Claude Agents parallel arbeiten lassen:

```bash
# Subagents dynamisch definieren
claude --agents '{"reviewer":{"description":"Reviews code","prompt":"You are a code reviewer"}}'

# Agent Teams mit tmux Display
claude --teammate-mode tmux
```

#### Git Worktrees

Isolierte Branches fuer parallele Entwicklung:

```bash
claude -w feature-auth           # Neuen Worktree erstellen
claude -w feature-auth --tmux    # Mit tmux-Session
claude --from-pr 123             # PR in Worktree auschecken
```

#### Vim Editor Mode

Vim-Style Editing aktivieren ueber `/config` → Editor Mode. Unterstuetzt Normal, Insert und Visual Mode mit Standard vim-Bindings (hjkl, w/e/b, dd, yy, p, etc.).

#### PR Review Status

Bei offenem PR zeigt Claude einen klickbaren Link im Footer:
- **Gruen**: Approved
- **Gelb**: Pending Review
- **Rot**: Changes Requested
- **Grau**: Draft
- **Lila**: Merged

Voraussetzung: `gh` CLI installiert und authentifiziert.

#### Session Recap

Nach einer Pause zeigt Claude automatisch eine einzeilige Zusammenfassung. Manuell mit `/recap` ausloesen.

#### Prompt Suggestions

Claude schlaegt nach jeder Antwort Folge-Prompts vor basierend auf git-History und Konversation. `Tab` oder `→` zum Uebernehmen.

#### Channels

Push-Events von Telegram, Discord, iMessage oder eigenen Webhooks in eine Session senden.

---

## Lizenz

Dieses Setup-Guide ist frei verfuegbar. Die einzelnen Tools haben eigene Lizenzen:
- gstack: MIT
- Superpowers: MIT
- claude-mem: AGPL-3.0
- GitNexus: MIT
- ECC: MIT
- Anthropic Skills: Siehe jeweilige LICENSE.txt
