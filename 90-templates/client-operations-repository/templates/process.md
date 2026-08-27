---
id: process-<short-name>
title: <Runbook name>
type: process
status: draft
summary: <Trigger, intended outcome and products/services covered.>
source_ids: []
owner: <process-owner>
created_at: <YYYY-MM-DD>
updated_at: <YYYY-MM-DD>
review_by: <YYYY-MM-DD>
tags: [class-confidential, process-runbook]
---

# <Runbook name>

## Purpose

State why and when the procedure runs and its successful outcome.

## Authority

State who may request, approve and execute; scope; maintenance window; and prohibited actions.

## Prerequisites

- <Approved ticket/change, access, evidence, backup, customer dependency and safety checks.>

## Procedure

1. <Numbered action and expected result.>
2. <Never include a secret value.>

## Verification

Specify authoritative read-after-write check, evidence retained, verifier and failure criteria.

## Exception and Escalation

State when to stop, contain, open/escalate a Freshdesk ticket, seek approval or involve the vendor/customer.

## Rollback or Containment

State safe reversal, access suspension, alternate procedure or truthful `not supported` boundary.

## Records Updated

List Markdown, Freshdesk, vendor, 1Password and finance records updated by the procedure.

## Relationships

- `operated-on` -> [[product-<name>|<Product>]]
- `implements` -> [[requirement-<name>|<Requirement>]]
- `escalates-to` -> [[<page-id>|<Support organization or owner>]]

## Evidence

Record last test/execution, result, source/ticket/change IDs and approved material.

