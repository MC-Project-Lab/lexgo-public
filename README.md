# LEXGO

Local-first privacy layer for documents before AI.

LEXGO is a prototype designed to prepare sensitive documents before they are used with tools such as ChatGPT, Claude, Copilot or Gemini. It focuses on detecting personal data, preserving useful context with placeholders, and letting the user review the output before sharing it.

This public repository is a product preview. The proprietary core is not included.

## Why

Many users paste real documents into LLMs:

- invoices
- contracts
- customer notes
- support tickets
- internal reports
- HR or administrative material

Those files can contain names, addresses, fiscal codes, IBANs, emails, phone numbers and internal references.

LEXGO sits before the AI step: it helps reduce exposure while keeping enough context for the model to work.

## What It Does

- detects personal and operational data in documents or pasted text
- replaces sensitive entities with coherent placeholders
- keeps context readable for LLM usage
- supports human review before export
- produces anonymized output and control reports
- follows a local-first operating model

## Placeholder Model

Instead of deleting everything, LEXGO keeps stable placeholders:

```text
Mario Rossi -> [NOME_1]
mario.rossi@example.com -> [EMAIL_1]
IT60X0542811101000000123456 -> [IBAN_1]
RSSMRA80A01H501U -> [CF_1]
```

This preserves relationships and roles without exposing the original values.

See [`examples/invoice-before-after.md`](examples/invoice-before-after.md).

## Example Use Cases

- prepare a customer invoice before asking an LLM to summarize it
- clean an internal note before sharing it with an AI assistant
- anonymize a support ticket while keeping the operational issue readable
- review PDF content before saving or sending an anonymized version

## Design Principles

- Local-first: documents should stay under user control.
- Human review: the user confirms what is masked.
- Context preservation: anonymization should not destroy usefulness.
- Placeholder consistency: the same entity keeps the same token.
- Auditability: users should know what was changed.

## Status

LEXGO is currently a proprietary prototype by MC Project Lab.

This repository is intentionally limited to:

- public positioning
- product notes
- synthetic examples
- early-access information

It does not include the implementation core, executable builds, private test files, OCR pipeline, PDF processing code, TCT integration code or real customer data.

## Early Access

For demo access:

**mcprojectlab@proton.me**

Official site:

https://www.mcprojectlab.com/lexgo.html

## License

See [`LICENSE`](LICENSE).
