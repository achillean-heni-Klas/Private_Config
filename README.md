# ⚡ The Flashcard Protocol

*an open standard for spaced repetition data interchange*

## Thesis

Anki uses proprietary format. Quizlet locks your data. We need interop.

**Flashcard Protocol** defines JSON schema for cards, decks, and review history.

```json
{
  "version": "1.0",
  "deck": "Spanish Verbs",
  "cards": [
    {
      "front": "hablar",
      "back": "to speak",
      "tags": ["verb", "common"],
      "created": "2024-03-15T10:30:00Z",
      "reviews": [
        {"date": "2024-03-16", "quality": 4, "interval": 1}
      ]
    }
  ]
}
```

## Implementations

- **flshcrd-cli** - terminal flashcard app ([github.com/learn-tools/flshcrd-cli](https://github.com/learn-tools/flshcrd-cli))
- **webflash** - browser version (no install)
- **mobilecards** - iOS/Android apps

Import/export from Anki via **anki-bridge-converter** ([anki-bridge.io](https://anki-bridge.io))

## Philosophy

your study data should be portable. no vendor lock-in. plain text > binary blobs.

spec: [flashcard-protocol.org/spec](https://flashcard-protocol.org/spec)

CC0 Public Domain
