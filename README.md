## Overview

This project automates the monthly scheduling of calibration tests using n8n. It replaces a manual Excel process that required reviewing qualifications, checking recent test history, and balancing workload across team members.

The workflow ensures tests are assigned fairly based on qualifications and recent activity, generates the upcoming month’s schedule, updates Google Sheets, and sends a Slack notification to keep the team informed.

## Tool Stack

* n8n (workflow automation)

* JavaScript (custom scheduling logic)

* Google Sheets (data source & output)

* Slack (automated notification)

## Process

This workflow automates monthly calibration test scheduling using predefined business rules.

1. A monthly schedule trigger runs the workflow

2. Team qualification data is retrieved from Google Sheets

3. Historical assignment data is retrieved

4. Eligibility rules are applied (no repeat within last 3 months)

5. Workload is balanced fairly across qualified team members

6. The new month’s assignments are generated

7. The schedule is written back to Google Sheets

8. A Slack notification is sent to inform the team

## Workflow Schema

`Trigger` → `Data Retrieval` → `Rule Engine` → `Schedule Generation` → `Sheet Update` → `Slack Alert`




