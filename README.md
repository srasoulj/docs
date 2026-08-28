# Rumizi help center

The public help site for [Rumizi](https://rumizi.com), built on
[Mintlify](https://mintlify.com) and published at
[guide.rumizi.com](https://guide.rumizi.com). It's linked from the vendor
workspace (**More → Guide**) and from the Rumizi site header.

Two audiences, two tabs:

- **For vendors** — restaurant owners and staff who edit and publish menus.
- **For diners** — people scanning a Rumizi QR code at a table.

A shared **Reference** tab holds the glossary, the public Rumizi surfaces
(drinks and steaks catalogs, restaurants directory), and the status page.

Pages are MDX with YAML frontmatter. Navigation lives in `docs.json`.

## Development

Install the Mintlify CLI:

```bash
npm i -g mint
```

Then, from the root of this repo (where `docs.json` lives):

```bash
mint dev              # local preview at http://localhost:3000
mint broken-links     # check every internal link
mint a11y             # accessibility check
```

If the dev server misbehaves, run `mint update` to get the latest CLI. A
page 404ing usually means you're not in a folder with a valid `docs.json`.

## Publishing

Changes deploy automatically when they land on `main`. Work directly on
`main` and push — this repo doesn't use feature branches or pull requests
for routine documentation updates.

Run `mint broken-links` before you push. There's no PR check to catch a
bad link after the fact.

## Writing

See [`AGENTS.md`](AGENTS.md) for voice, components, and what does and
doesn't belong on this site. Internal engineering documentation lives in
the `rumizi` repo under `docs/` and stays private.

## Need help?

- [Mintlify documentation](https://mintlify.com/docs)
- Rumizi support: [hi@rumizi.com](mailto:hi@rumizi.com)
