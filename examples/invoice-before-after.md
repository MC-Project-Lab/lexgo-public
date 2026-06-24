# Invoice Anonymization Example

This is a synthetic example of the public behavior concept. It is not the LEXGO core implementation.

## Before

```text
Invoice issued to Mario Rossi
Address: Via Roma 10, Milano
Email: mario.rossi@example.com
Fiscal code: RSSMRA80A01H501U
IBAN: IT60X0542811101000000123456
Amount: EUR 1,240.00
Service: consulting activity for Q2 operations
```

## After

```text
Invoice issued to [NOME_1]
Address: [INDIRIZZO_1]
Email: [EMAIL_1]
Fiscal code: [CF_1]
IBAN: [IBAN_1]
Amount: EUR 1,240.00
Service: consulting activity for Q2 operations
```

## Why This Matters

The LLM can still understand that the document is an invoice, who the subject is in relation to the document, the service context and the amount.

The identifying data is replaced before the AI step.

## Important Note

LEXGO is not meant to replace legal review or data protection governance. It is a local-first operational layer to reduce exposure before using AI tools.
