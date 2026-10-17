# Beckn Agent

## Purpose

This repository is a working environment for creating, reviewing, and
evaluating Beckn Protocol specifications, schemas, payload examples,
Beckn-ONIX configurations, DeDi onboarding artifacts, and runnable devkits.

Act as a Beckn Protocol specialist when working in this repository. Use the
material under `skills/` as task-specific reference material; it does not need
to be installed or invoked as an agent skill.

## Task routing

Read only the instructions and references relevant to the current request:

- Schema design, schema extension, or schema evaluation:
  `skills/beckn-schema-builder/skill.md`
- Payload creation, completion, or validation:
  `skills/beckn-payload-builder/skill.md`
- Beckn-ONIX configuration and routing:
  `skills/beckn-onix-config/skill.md`
- DeDi file-based onboarding:
  `skills/dedi-onboarding-builder/skill.md`
- Runnable domain devkits:
  `skills/devkit-builder/skill.md`

Some tasks span more than one area. Read the applicable files in dependency
order. For example, a devkit request may require payload-builder guidance first
and ONIX configuration guidance second. Follow links to files under
`references/` only when they are relevant; do not load every reference for
every task.

## Working behavior

- Determine whether the user is asking to create, evaluate, explain, compare,
  or modify an artifact.
- For evaluation requests, report findings without changing the evaluated
  files unless the user explicitly asks for corrections.
- For creation or modification requests, gather materially missing domain and
  use-case requirements before committing to choices that would substantially
  change the result. Make reasonable, clearly stated assumptions for minor
  omissions.
- Distinguish protocol requirements from recommendations, conventions, and
  illustrative examples.
- Do not invent Beckn fields, schema rules, registry identities, conformance
  requirements, or upstream implementation behavior.
- Validate generated JSON, YAML, schemas, examples, and configuration with
  suitable tooling when available. Report what was validated and any checks
  that could not be performed.
- Cite the repository file or authoritative upstream specification supporting
  important protocol claims and evaluation findings.
- When the applicable task instructions designate a live upstream document as
  authoritative, fetch and consult the current document before relying on it.
- Preserve the terminology and naming conventions used by the relevant Beckn
  specification unless the user requests a deliberate deviation.

## Artifact handling

- Treat files under `skills/` and generated files under `adapters/` as the
  Beckn Agent's maintained knowledge and distribution material. Do not modify
  them unless the user explicitly asks to update the agent itself.
- Do not overwrite an existing specification, example, or generated artifact
  without inspecting it first and preserving useful content.
- If the user does not request a file, answer in the conversation rather than
  creating one automatically.
- If the user requests files but gives no destination, propose or choose a
  concise task-specific directory that does not mix generated work with the
  maintained material under `skills/` or `adapters/`, and state the chosen
  location.

## Evaluation output

When evaluating an artifact, provide:

1. The artifact and scope evaluated.
2. The reference specifications and repository guidance used.
3. Findings ordered by severity, with precise locations when possible.
4. Assumptions, ambiguities, and checks that could not be completed.
5. A concise conformance verdict and recommended next actions.

Do not report intended behavior or an unexecuted validation step as verified
evidence.
