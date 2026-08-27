# Documentation policy

**Owner:** <repository-owner>  
**Status:** Draft template  
**Review by:** <YYYY-MM-DD>

## Purpose

Keep company knowledge findable, authoritative, reviewable and appropriately separated from application code, client records, secrets and restricted source documents.

## Placement rule

Place a durable document in the functional area accountable for maintaining it. Use `80-initiatives/` only to coordinate temporary cross-functional work. When an initiative closes, move or link each durable output to its owning functional area.

## Required metadata

Every governing or operational document should identify:

- title and stable document ID;
- domain and document type;
- status and authority;
- owner and approver where applicable;
- sensitivity;
- effective and review dates;
- superseded and related records.

## Controlled values

- **Type:** strategy, policy, plan, framework, specification, runbook, checklist, register, template, record, reference.
- **Status:** draft, working, approved, superseded, archived.
- **Authority:** governing, supporting, informational.
- **Sensitivity:** public, internal, confidential, restricted.

Folder paths do not grant or restrict access. Restricted information belongs in an access-controlled system appropriate to the record type.

## Versioning

Use stable filenames for living documents and Git history for revisions. Use dates in filenames for event records, reporting periods and immutable snapshots. Do not create `final-v2-final` filenames.

## Indexing

The root README is a company map, not a list of every file. Each functional README lists its governing documents, active plans, owner and related systems.

## Archive

Retain superseded material when it has decision, legal or historical value. Mark its status and replacement before moving it to `99-archive/`. Archiving must not be used as a substitute for required secure deletion.

