# Vocabulary Extraction Feature Set

## Core Capabilities

### File Upload
- Accepts common text-based formats including `.txt`, `.docx`, and `.pdf`.
- Provides a clear upload flow so users can supply source documents.

### Text Extraction
- Extracts text from uploaded documents.
- Supports OCR for scanned PDFs to ensure text can be captured even when not selectable.

### Advanced Vocabulary Extraction
- Detects collocations, idioms, phrases, and phrasal verbs.
- Checks extracted collocations/phrases against the user’s dictionary:
  - If present, records the matching definition number (and example number for collocations/phrases).
  - If absent, breaks the collocation/phrase into its components.
- Extracts words used in collocations, idioms, phrases, and phrasal verbs **only** when they retain their original meaning.
- Extracts remaining single words that are not part of a qualifying multi-word expression.
- Avoids re-adding words already extracted with the same meaning.
- For every extracted word, records:
  - The matching definition number from the user’s dictionary.
  - The source page number.

### Downloadable Vocabulary List
- Offers a downloadable `.txt` output of the generated vocabulary list.

## Output Requirements
- Every extracted entry must include:
  - Term or phrase.
  - Source page number.
  - Dictionary definition number.
  - Example number (when applicable for collocations/phrases).
- Entries that are repeats with the same meaning are omitted from the newly generated list.
