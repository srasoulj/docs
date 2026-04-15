# Rumizi help center — docs project

Public help site for Rumizi, built on [Mintlify](https://mintlify.com).
Pages are MDX with YAML frontmatter; navigation lives in `docs.json`.

Source-of-truth engineering docs live in the `rumizi` repo under
`docs/`; this site is the diner- and vendor-facing rewrite. Do **not**
copy internal engineering docs (super-admin, operations, rewrite-parity,
architecture) into this repo — those stay private.

## Audience

Two audiences, two tabs:

- **For vendors** — restaurant owners and staff editing menus.
- **For diners** — people scanning a Rumizi QR code at a table.

A shared **Reference** tab holds the glossary and status page.

## Commands

- `mint dev` — local preview at `http://localhost:3000`.
- `mint broken-links` — check internal links before a PR.
- `mint a11y` — accessibility check.

## Writing style

- Second person ("you") for instructions.
- First person "I" when Rumizi itself is speaking (copy and tone follows
  Rasoul's voice — see `rumizi/docs/content/copywriting-guidelines.md`).
- Sentence case headings ("Set up your first menu").
- Bold for UI elements ("Tap **Publish**").
- Code formatting for file names, URLs, env-style values.
- Short paragraphs. One idea per sentence.

## Components

Prefer Mintlify's built-ins over raw HTML:

- `<Card>`, `<Columns>` for navigation grids.
- `<Steps>`, `<Step>` for sequential instructions.
- `<Tabs>`, `<Tab>` for parallel options.
- `<AccordionGroup>`, `<Accordion>` for FAQ-style content.
- `<Note>`, `<Tip>`, `<Warning>`, `<Info>` for callouts.

## Content boundaries

Don't document:

- Super-admin features.
- Database schema, migrations, or server actions.
- Internal pipelines, feature flags, or AI prompt engineering.
- Rewrite-parity audits.

If you find yourself writing any of the above, stop — it belongs in the
`rumizi` repo's internal `docs/` folder, not here.
