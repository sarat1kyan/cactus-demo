
# CACTUS — Product Design Brief (MVP → Management Console)

# 1. Executive summary
CACTUS is a deep-hardening security & forensics product that continuously enforces compliance, performs deep forensic analysis, and visualizes network topology. Primary users are SOC analysts, sysadmins, forensic specialists, and enterprise IT teams. The first-stage MVP to deliver is a full management console (web) containing everything in the supplied `demo.html`; the agent UI is planned for a later stage. (You requested we keep only the product name Cactus from the demo branding.)

Differentiator: CACTUS is faster (~19.3% faster/accurate average benchmark included tools) and includes integrated real-time hardening, smart forensics and FIM/DLP for configuration files.



# 2. Deliverables
Must deliver (MVP / Stage 1):
- High-fidelity interactive Figma prototype (desktop-first, responsive to tablet).  
- Clickable flows for the critical user journeys (see Section 5).  
- Design system / component library (Figma components + tokens: color, spacing, typography, elevation).  
- Exportable assets: SVG icons, PNG placeholders, CSS token snippet (vars), example HTML snippets matching the design system.  

Should deliver (stage 1):
- Low-fidelity mobile wireframes for the highest-priority screens.  
- Accessible color palette and contrast checks (WCAG AA minimum).  

Nice-to-have (future / optional):
- Dark / light theme toggle with tokens.  
- Animations spec and microinteraction examples.



# 3. MVP scope — features present in `demo.html` (to match/implement)
Implement everything visible and functional in the demo, including but not limited to:

- Global navigation / top bar with login/logout and user info.  
- Tab navigation with screens: Dashboard, Threats, Forensics, Compliance, Network, Agents, Settings.  
- Dashboard cards (Threats Blocked, System Health, Active Threats, Compliance Score).  
- Recent Alerts table.  
- Threat Management: File scanner + URL scanner forms.  
- Digital Forensics: Memory analysis & PCAP upload + Recent Analyses table.  
- Compliance screen showing security settings and compliance overview.  
- Network Topology visualizer with controls (refresh, fit, layout, physics toggle).  
- Agents management list with agent actions (sysinfo, processes, ping, view results).  
- Login modal & Agent output modal (terminal-style output).



# 4. Visual & brand direction
- Name: Cactus  
- Tone: Professional enterprise security product — clear & information-dense.  
- Palette: Refined, modern UI, accessibility compliant.  
- Typography: Legible UI font + monospaced type for terminal.  
- Iconography: Short actionable labels + consistent icons.



# 5. Key screens & components
Screens
1. Dashboard  
2. Threat Management  
3. Digital Forensics  
4. Compliance  
5. Network Topology  
6. Agents  
7. Settings  
8. Modals (login user/sso, output, confirm)

Components
- Nav bars, tables, cards, upload forms, graph canvas, terminal output pane, buttons, dialogs.



# 6. API contract notes
MVP endpoints referenced in demo.html:
- `/api/dashboard/overview`
- `/api/dashboard/alerts`
- `/api/threats/detected`
- `/api/forensics/analyses`
- `/api/settings/security`
- `/api/agents`
- `/api/network/topology`
- `/api/auth/login`



# 7. Three UX flows
### Flow A — Investigate Alert  
Dashboard → alert → forensic analysis → results & incident options.

### Flow B — Run File Scan  
Threats → upload → progress → results & actions.

### Flow C — Agent Command & Output  
Agents → command → queued → fetch output in terminal view.
