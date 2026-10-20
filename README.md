# Cabinet Project Management & AI Automation Engine

An n8n portfolio project integrating **ClickUp**, **Gmail**, and **OpenAI** to support cabinet-installation project monitoring, task alerts, team reporting, and AI-assisted design review.

## Features
- Identifies overdue, due-soon, high-priority, and at-risk ClickUp tasks and emails a project risk alert.
- Detects incomplete tasks inactive for 3 or more days and emails stalled-task alerts.
- Produces daily task check-ins and weekly project summaries.
- Routes eligible design-review tasks to a separate AI review workflow.
- The AI review flags missing measurements, material specifications, clearances, coordination concerns, and approval requirements; it emails its findings and posts an advisory ClickUp comment. **A human must verify before production.**

## Architecture
- `workflows/cabinet-project-management.json` — main scheduled workflows and routing.
- `workflows/ai-cabinet-design-review.json` — AI-assisted design review sub-workflow.

## Demo
Add the public-viewable Loom demonstration URL here after confirming its sharing permissions.

## Setup (templates; not ready to run without configuration)
1. Import the **sub-workflow first**, then import the main workflow into n8n.
2. Connect your own ClickUp, Gmail, and OpenAI credentials.
3. Replace `REPLACE_WITH_YOUR_CLICKUP_*_ID` with the correct ClickUp workspace, space, and list IDs.
4. In the main workflow's **Run AI Cabinet Design Review** node, select the newly imported sub-workflow.
5. Replace `your-email@example.com` with the intended alert recipient.
6. Review schedules and workflow timezone; test with non-sensitive sample tasks before activating.

## Safety and limitations
- This is a sanitized demonstration export. Account references, recipient email addresses, pinned execution data, and deployment identifiers have been removed.
- Importing does not prove the workflow will run correctly in another environment; configure and test before use.
- AI design assessments are advisory and **do not constitute engineering certification or production approval**.
- Screenshots and Loom recordings should be checked for private data before public sharing.

## Tools
n8n · ClickUp · Gmail · OpenAI
## 🎬 Video Demonstration

Watch the 3-minute demonstration of the Cabinet Project Management & AI Automation Engine.

[▶️ Watch Loom Demo](https://www.loom.com/share/135fed90aa07496b8c9eb47a199ba0e5)
