# PolicyPilot — AI Compliance Intelligence

A dashboard for AI compliance and regulatory risk monitoring, featuring real-time policy status, risk assessment, violation management, and embedded analysis tools. Designed as part of Hackfest Hackathon.

---

## Overview

**PolicyPilot** lets compliance teams track, analyze, and manage organizational adherence to major data privacy and regulatory standards (GDPR, CCPA, HIPAA, DPDP, SOC 2, ISO 27001). The UI features dynamic reporting (charts, alerts), violation feed, audit logs, manual override workflow, and integration with AI for document policy extraction and incident analysis.

### Key Features

- **Compliance Dashboard:** Visualizes health metrics, current policy statuses, active violations, and risk severity.
- **Policy Document AI Extraction:** Upload policy PDFs (up to 50MB); AI parses and enumerates actionable compliance rules, each with risk scores.
- **Violation Management:** Monitor active, flagged, reviewed, and remediated violations. Features severity (Critical, High, Medium, Low) grading and oversight tools.
- **Manual Override Workflow:** Detailed modal for compliance officer audit, legal/false positive flagging, DPO exceptions, with reason tracking and audit trail.
- **Red Team / Blue Team Analysis:** Simulated attack/defense scenarios with dynamic, AI-powered summarization for breach attempts, policy bypasses, and mitigation rates.
- **Databases Section:** Lists major sources (e.g. compliance_db, hr_mysql); allows test/scan, addition/removal, and shows current test status.
- **Audit Trail:** Change tracking for settings and override actions, supports log export and clearance.
- **Advanced UI:** Responsive design with rich charts, glassmorphism, Aurora backgrounds, and Three.js-powered 3D logo.

---

## Technologies Used

- **HTML5 & CSS3:** Grid and Flexbox layouts, custom properties, advanced animations, glassmorphic styling
- **JavaScript (Vanilla):** Interactive logic, modals, policy extraction, charts, team analysis, override workflow
- **Three.js:** For canvas-based 3D logo and effects
- **No Build Step:** Fully static app, no framework required

---

## Structure & Main Components

- `index.html`: Single-page app containing all markup, scripts for UI, logic (policy upload, analysis, compliance functions), and main pages.
    - **Dashboard Section:** Health donut charts, metric tiles, violation feed, policy listing.
    - **Policy Upload Section:** PDF drag-and-drop, rule extraction (AI prompt and logic for different regulations, risk ranking).
    - **Violation Feed:** Table of live issues, status controls, "Explain" and "Override" modals providing context, reason tracking, and reviewer log.
    - **Manual Overrides:** Modal with recommended reasons (Legal Hold, False Positive, Exception by DPO, Remediation in progress) and freeform explanation; all actions audit logged.
    - **Team Analysis:** Red Team/Blue Team scenario breakdowns with dynamic, AI-generated assessment and key metrics.
    - **Database Panel:** Add, scan, remove databases; shows test status and compliance metadata.
    - **Audit Trail:** Logs all manual changes, override actions, settings updates—available for download.

- `system_prompt.txt`: Contains compliance domain references (GDPR, CCPA, HIPAA, DPDP, SOC 2, ISO 27001), initialization behavior, and principles for automated rule contextualization.

---

## Supported Compliance Domains

- **GDPR, CCPA, HIPAA, DPDP Act 2023, SOC 2 Type II, ISO 27001**
- Principles: Data minimization, purpose limitation, retention limits, access controls

### Example Rules Extracted

- **GDPR-12a · Data Retention · CRITICAL:** "All customer PII must be deleted or anonymized after 5 years from the date of last transaction."
- **AML-001 · Transaction Threshold · CRITICAL:** "Any single transaction exceeding $10,000 USD must be flagged for CTR filing."
- **IRD-5 · Bias Monitoring · CRITICAL:** "Recommendation system bias audit overdue by 47 days; requires immediate retraining."
- **DR-5b · Proactive Anonymization:** "Proactive scheduling 90 days prior to 5-year limit required by policy."

---

## Local Development

No build step; just clone and open:

```bash
git clone https://github.com/paarthbhatt/Hackfest_Hackathon_Project.git
cd Hackfest_Hackathon_Project
# Open index.html in your browser
```
---

## Usage Guide

1. **Upload Policy PDFs:** Use the panel; AI extracts and lists rules, risk level, actionable items.
2. **Explore Dashboard:** Review live compliance metrics, health charts, violation feed.
3. **Violation Management:** Click "Explain" for details, "Override" for audit-modal; reasons logged.
4. **Red/Blue Team Analysis:** Run scenarios to test policy resilience, review data-driven summary.
5. **Audit Trail:** Download or clear log as needed.

---

## Contributing

- All code is HTML/CSS/JS for rapid prototyping; contribute via pull requests.
- Code comments are concise; please annotate function logic when extending.
- Suggest new compliance domains or override reasons via issues or PRs.

---

## License

MIT License (see LICENSE file if present)

---

## Author

**Parth Bhatt** — Hackfest Hackathon, 2024-2026
