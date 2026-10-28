# SOC Brute-Force Investigation

**Analyst:** Diya Kelvin Powei

## Overview
A hands-on SOC Analyst portfolio project investigating Windows Security logs, failed authentication events, and basic detection logic.

## Objectives
- Examine Windows Event ID 4625.
- Interpret authentication event fields.
- Develop a basic repeated-failure detection approach.
- Document findings and incident response recommendations.

## Tools
- Windows Event Viewer
- Windows Security logs
- Markdown
- GitHub

## Project Structure
- `investigation/` — incident investigation report
- `detections/` — detection logic and limitations
- `screenshots/` — visual evidence from the lab
- `logs/` — labelled sample authentication data

## Initial Findings
Ten Event ID 4625 events were observed in the filtered Security log during the initial review. The events were spread across October 26–28, 2026.

The initial evidence confirms failed logons, but does not independently establish a brute-force attack.

## Ethical Scope
This project analyses logs from my own Windows environment. Any synthetic records are labelled as examples and are not presented as real observations.

## Next Steps
- Correlate failed logons with successful logons.
- Review relevant account and process details.
- Refine detection thresholds and document false-positive risks.
- Expand the investigation with additional validated evidence.
