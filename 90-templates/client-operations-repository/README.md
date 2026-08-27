# Client operations repository template pack

**Version:** 0.1  
**Date:** 2026-08-26  
**Status:** Design source for the future repository generator; not a production workspace by itself

This pack defines the Markdown contract that a Dirtyworks.ai client repository generator and internal interface should implement. It is designed to fit the current `personal-wiki` version-2 page schema and the `kgmd` directory/MCP model without modifying either project first.

## Contents

- [`recipe.yaml`](recipe.yaml) — proposed personal-wiki recipe identity and version.
- [`config/schema.yaml`](config/schema.yaml) — proposed personal-wiki page types, sections, states and review rules.
- [`config/connections.yaml`](config/connections.yaml) — empty source-connection skeleton; add only approved client-local connections.
- [`config/prompts/ingest.md`](config/prompts/ingest.md) — proposed client-operations ingestion/synthesis preamble.
- [`kgmd-config.yaml.example`](kgmd-config.yaml.example) — restricts the derived graph to published `wiki/` content.
- [`gitignore-additions.txt`](gitignore-additions.txt) — derived kgmd and interface state that must not be committed.
- [`templates/`](templates/) — copyable authored-page templates; keep this directory outside the published `wiki/` corpus.

## Intended generated repository

Initialize the actual workspace through `personal-wiki`, then apply the client-operations recipe/configuration rather than copying this directory wholesale.

```text
dw-client-c0007/
├── config/
│   ├── wiki.yaml
│   ├── schema.yaml
│   ├── connections.yaml
│   └── prompts/ingest.md
├── raw/                       # approved imported originals only
├── wiki/                      # flat published authoritative pages
├── changes/                   # personal-wiki review artifacts
├── state/                     # personal-wiki tracked and derived state
├── templates/                 # authored-page templates; excluded from graph
├── .kgmd/
│   ├── config.yaml            # may be tracked if it contains no secret
│   └── graph.db               # derived, sensitive, untracked
└── .gitignore
```

## Tool-generator requirements

The future generator should:

1. require a stable non-sensitive customer ID;
2. create a new private Git repository rather than a subdirectory in a shared client repository;
3. initialize `personal-wiki` and apply the client-operations schema/prompt;
4. create the authored account page from sponsor-approved inputs;
5. configure `kgmd` to index only `wiki/`;
6. install ignore/secret-scanning rules before the first commit;
7. reject secrets and disallowed classifications from the drop zone;
8. require human review before generated findings reach the published branch and explicit promotion before a finding becomes an authored operational record;
9. run schema, link, freshness and source-lineage checks;
10. add deterministic authored-page checks for required sections, owner, review date, one classification tag and controlled relationship syntax;
11. record repository, Freshdesk, 1Password, contract and finance IDs in the account page;
12. test fresh-clone recovery and cross-client isolation;
13. emit no raw customer content to logs or analytics.

The current kgmd `corpus.include` option scopes discovery to `wiki/` but does not exclude personal-wiki's reserved `index.md` and `log.md`, parse page frontmatter as metadata, or parse controlled relationship bullets deterministically. The generator/interface wrapper must supply those behaviors before production use; do not add unsupported configuration keys and assume kgmd honors them.

## Template conventions

- Replace every `<placeholder>` before placing a page under `wiki/`.
- Filename must be `<id>.md` and remain flat under `wiki/`.
- Use exactly one `class-*` tag.
- Active operating records require `owner` and `review_by`.
- Generated ingestion targets `finding` and `source`; it must not target authored operational page types.
- Cite registered evidence with `src-NNNN` where available.
- Use the controlled relationship form: ``- `predicate` -> [[page-id|Title]]``.
- Link external authorities using non-secret stable record IDs/URLs appropriate to the repository's access policy.
- Never put a password, recovery code, API secret or token in a template/page.

See the [Markdown client repository operating model](../../06-client-delivery/client-operations-platform/markdown-client-repository-operating-model.md) for authority, security, ingestion, interface and migration rules.
