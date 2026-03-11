# AGENTS.md

Instructions for AI agents working in this repository.

---

## Folder Structure

All writeups must follow this hierarchy:

```
<contest-name>/<category>/<challenge-name>/
├── README.md       # writeup (copied from templates/TEMPLATE.md)
├── solve.py        # solve script (if applicable)
└── files/          # challenge attachments (if any)
```

**Examples:**
```
lactf-2026/web/bobles-and-narnes/
├── README.md
├── solve.py
└── files/

apoorvctf-2026/osint/journey/
└── README.md
```

Each contest lives at the root level with its own `README.md` (copied from `templates/CONTEST_TEMPLATE.md`).

## Naming Conventions

- **Contest folders:** lowercase, hyphenated, include year — e.g., `lactf-2026`, `apoorvctf-2026`
- **Challenge folders:** lowercase, hyphenated — e.g., `bobles-and-narnes`, `journey`
- **Category folders:** use only the defined categories below (lowercase, no spaces)

## Valid Categories

`web` · `pwn` · `crypto` · `rev` · `misc` · `forensics` · `osint` · `stego` · `ai` · `cloud`

Do not create new categories without updating `README.md`.

## Adding a New Contest

1. Create `<contest-name>/` at the repo root
2. Copy `templates/CONTEST_TEMPLATE.md` → `<contest-name>/README.md` and fill in metadata
3. Add a row to the **Contests** table in the root `README.md`

## Adding a New Writeup

1. Create `<contest>/<category>/<challenge-name>/`
2. Copy `templates/TEMPLATE.md` → `<contest>/<category>/<challenge-name>/README.md`
3. Fill in all fields: contest, category, points, difficulty, flag, description, solution
4. Add a row to the **Solved Challenges** table in `<contest>/README.md`
5. Increment the writeup count in the root `README.md` contests table

**Examples:**
- LA CTF 2026 web challenge → `lactf-2026/web/bobles-and-narnes/README.md`
- ApoorvCTF 2026 osint challenge → `apoorvctf-2026/osint/journey/README.md`

## Templates

Always use the templates in `templates/` — do not invent new formats.

| Template | Purpose |
|----------|---------|
| `templates/TEMPLATE.md` | Individual challenge writeup |
| `templates/CONTEST_TEMPLATE.md` | Per-contest README |

## File Hygiene

- Do **not** commit large binaries (`.iso`, `.vmdk`, `.ova`)
- Keep challenge attachments inside the challenge's `files/` subfolder
- Do not commit credentials, tokens, or `.env` files

## What NOT to Do

- Do not create category folders outside the valid list above
- Do not skip updating `README.md` files after adding a writeup
- Do not rename or restructure existing contest/challenge folders without user confirmation
- Do not add new top-level files or folders not defined in this structure without user confirmation
