---
id: incident-<client-id>-<date>-<short-topic>
title: <Non-sensitive incident title>
type: incident
status: open
summary: <Current impact, containment and state without unnecessary sensitive detail.>
source_ids: []
owner: <incident-owner>
created_at: <YYYY-MM-DD>
updated_at: <YYYY-MM-DD>
review_by: <YYYY-MM-DD>
tags: [class-restricted, incident-<service|security|privacy|vendor>]
---

# <Incident title>

## Detection

Record detected/reported time, channel, reporter role and confidence. Link the authoritative incident/Freshdesk record.

## Impact

Record confirmed and possible systems, users, data and service effects separately.

## Containment

Record authority, actions, timestamps, verification and remaining exposure.

## Timeline

- **<timestamp>:** <fact/action/decision and source>

## Cause

Record confirmed cause, contributing factors or `under investigation`; do not speculate as fact.

## Corrective Action

Record immediate and longer-term actions, owners, due dates and verification.

## Relationships

- `applies-to` -> [[<page-id>|<Service or product>]]
- `produced-by` -> [[<page-id>|<Related change/process>]]
- `escalates-to` -> [[<page-id>|<Incident contact/organization>]]

## Customer Communication

Link approved Freshdesk/incident communications and accountable decision owner.

## Recurrence Prevention

Link approved requirement, process, risk or change updates.

## Evidence

Link controlled evidence; do not paste secrets or unnecessary personal/customer content.

