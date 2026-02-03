# Automate-a-Real-Workflow-End-to-End
Agentic AI 

![image](https://github.com/Ishita95-Harvard/Automate-a-Real-Workflow-End-to-End/blob/main/Screenshot%20(865).png)

---

## Phase 1 connections:
Calendly Trigger -> Create Lead Record -> Identify Company API -> ContactIQ Enrichment -> Download Leads API -> Branding Company API -> Search Project API -> Lead Finders API -> Store in Database

## Phase 2 connections (starting from Store in Database or from a meeting recording trigger?):
In the first workflow, Phase 2 started after Phase 1. In the second workflow, it seems Phase 2 starts after the meeting.

We'll connect: Store in Database -> Transcript Transcription API (but note: in reality, the transcript processing happens after the meeting, so maybe we need a trigger for when the meeting recording is available).

Alternatively, we can have a separate trigger for the transcript. For simplicity, we'll follow the first workflow and assume the transcript is available after the meeting.

So: Store in Database -> Transcript Transcription API -> Organize Transcript API -> Create Google Doc -> Update Language Doc API -> Meeting Classifier AI

## Phase 3 connections:
Meeting Classifier AI -> Discovery Content API -> Presentation Content API -> Generate Proposal Document

Dashboard connections:
We want the dashboard to receive data from various points. We'll connect:
- Store in Database -> Grouped Contacts Chart (to get contact data for the chart)
- Scheduled Outputs Trigger -> Dashboard Aggregator (to trigger regular updates)
- Grouped Contacts Chart -> Dashboard Aggregator

