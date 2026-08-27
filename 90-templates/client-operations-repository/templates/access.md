---
id: access-<identity-or-role>-<product>
title: <Identity or role access to product>
type: access
status: requested
summary: <Who or what requires which role, for what purpose, and current state.>
source_ids: []
owner: <access-owner>
created_at: <YYYY-MM-DD>
updated_at: <YYYY-MM-DD>
review_by: <YYYY-MM-DD>
tags: [class-restricted, control-access]
---

# <Access record title>

## Access Record

- **Identity/service identity:** <named identity; minimize personal information>
- **Product/tenant:** <link>
- **Role/scope/purpose:** <least privilege>
- **1Password item reference:** <reference only; never the secret>
- **Created/expires/review dates:** <dates>

## Approval

Record customer approver, Dirtyworks.ai requester, authorization evidence and conditions.

## Verification

Record native entitlement checked, MFA result, verifier, date and exceptions.

## Revocation

Name revocation owner, trigger, procedure and completed evidence when applicable.

## Relationships

- `applies-to` -> [[product-<name>|<Product>]]
- `approved-by` -> [[person-<name>|<Approver>]]
- `implemented-by` -> [[process-<name>|<Access process>]]

## Exception

Record shared-account/vendor limitation, risk owner, compensating control and remediation expiry—or `None`.

## Evidence

Link customer authorization and native verification without including sensitive values.

