---
name: INTRSPOT BI Platform — Project Overview
description: Core description of the INTRSPOT business intelligence platform being built in this working directory
type: project
originSessionId: d937747d-6ea2-4718-96d0-079067732748
---
INTRSPOT is an AI-powered Business Intelligence platform consisting of three main components:

1. **bi-agent/backend** (Python/FastAPI) — The core AI engine using Claude claude-opus-4-6. Contains:
   - `agent.py`: Agentic loop (max 20 iterations, 15 tool calls) that accepts a DataFrame + user question
   - `tools.py`: 6 Claude-callable tools: `analyze_data`, `run_python`, `generate_chart`, `generate_powerbi_code`, `generate_tableau_code`, `generate_report`
   - `tableau_publisher.py`, `data_loader.py`, `workbook_builder.py`: Tableau integration utilities
   - Bilingual (Arabic + English) — system prompt supports both languages

2. **bi-agent/mcp_server** (`intrspot_mcp.py`) — FastMCP server exposing 6 MCP tools to Claude directly:
   - `load_file`, `analyze_data`, `publish_to_tableau`, `list_tableau_content`, `quick_stats`, `list_datasets`

3. **bi-platform** (React + TypeScript + Vite + Framer Motion) — Marketing/landing page with sections: Hero, Services, HowItWorks, Stats, Pricing, Testimonials, CTA, Blog

**Why:** Building a SaaS BI platform that lets users upload Excel/CSV data and get AI-generated insights, charts, Power BI DAX code, and Tableau calculated fields — plus direct publish to Tableau Server/Online.

**How to apply:** When working on this project, understand it's a bilingual (AR/EN) platform. The agent is designed for efficiency (≤15 tool calls). Tableau integration is a key differentiator.

## Current Status
- Deployment: Planning stage — cloud provider not yet selected
- Competitor research: Pending (niche not yet defined)
- Architecture PDF generated at `output/bi-agent-architecture.pdf`
