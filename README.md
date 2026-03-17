# ASCII Wireframe Skill for Claude

> Created by [Vitalik Pestov](https://www.linkedin.com/in/vitalipestov)

A Claude skill that forces a **wireframe-first** workflow: draw the structure in ASCII before writing any code. This eliminates guesswork about layout, proportions, and hierarchy — you approve a visual blueprint, then Claude builds it exactly.

## The Problem

When you ask Claude to "build me a dashboard" or "create a landing page," it fills in hundreds of layout decisions on its own — sidebar width, chart proportions, column count, button placement. The result looks polished but rarely matches what you had in mind. You spend 30 minutes fixing things that should have been right from the start.

## The Solution

This skill introduces a three-step process: **Sketch → Iterate → Build**.

1. **Sketch** — Claude draws an ASCII wireframe with explicit proportions, labels, and sample data. No code.
2. **Iterate** — You request changes to the wireframe. Cheap and instant — no code to rewrite.
3. **Build** — Claude implements the approved wireframe as an exact specification.

## What It Covers

- **Web interfaces** — dashboards, apps, landing pages with explicit grid proportions
- **Presentations** — slide-by-slide wireframes with distinct layout types per slide
- **Database schemas** — ER diagrams with tables, columns, types, and FK relationships
- **Automation workflows** — n8n/Zapier flowcharts with ALL branches including error paths
- **Email templates, mobile screens, multi-step forms**

## Example

Ask Claude to build a SaaS dashboard. Instead of jumping to code, it produces:

```
+----------------------------------------------------------------------+
| NAVBAR                    [Search]              [Bell] [Avatar]      |
+------+---------------------------------------------------------------+
|      | +----------------+ +----------------+ +----------------+      |
| SIDE | | Revenue        | | Users          | | Churn          |      |
| BAR  | | $48,200        | | 1,842          | | 2.1%           |      |
| 15%  | +----------------+ +----------------+ +----------------+      |
|      | +----------------------------------+ +--------------------+    |
| Dash | | Revenue Over Time                | | Traffic Sources    |    |
| Ana  | | line chart — 60% width           | | pie — 40%          |    |
| Memb | +----------------------------------+ +--------------------+    |
| Rev  | +----------------------------------------------[+ New]---+    |
| Set  | | Recent Members                                        |    |
|      | | Name    | Plan | Date       | Status                  |    |
|      | | Alice   | Pro  | 2026-02-28 | * Active                |    |
|      | +--------------------------------------------------------+    |
+------+---------------------------------------------------------------+
```

Every proportion is visible. Every element is labeled. You approve it, then Claude builds it.

## Installation

Download `ascii-wireframe.skill` from the [Releases](../../releases) page and install it in Claude Desktop or Claude Code.

Or copy `SKILL.md` into your skills directory.

## Key Prompts

**Step 1 — Generate wireframe:**
```
Before writing any code, create an ASCII wireframe of [your thing].
Use box-drawing characters and arrows for flow.
Do not write any code. Output only the ASCII.
```

**Step 2 — Iterate:**
```
Make the sidebar 20% instead of 15%. Add a search bar to the table. Redraw.
```

**Step 3 — Build:**
```
Build this using React + Tailwind. Match the wireframe exactly.
```

## License

MIT
