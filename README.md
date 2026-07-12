# Route Planner — Route Hub

Curated routes for the [Route Planner](https://github.com/BlackDeath-Osrs/route-planner) RuneLite plugin.

Browse and install routes from inside the plugin: **Import ▾ → Browse Route Hub**. Submitting a
route works the other way — the plugin never uploads anything, so sharing a route means opening a
pull request here.

## How to submit a route

1. **Build your route** in Route Planner, then export it (**Export ▾ → Export to file**).
2. **Fork this repo** and add your route:
   - Place the exported JSON in `routes/<your-route-id>.json`.
   - Add a **48×48 PNG icon**, under **20 KB**, at `icons/<your-route-id>.png`. A plain, simple
     image reads better than a busy one at that size.
   - Add an entry for your route in `index.json` (see the format below).
3. **Open a pull request.** Every submission is reviewed before it appears in the Hub — this keeps
   the catalog safe, since routes are downloaded and installed directly into other people's plugins.

## What gets checked in review

- **No links of any kind** in any text field (route/section/step names, notes, item lists,
  NPC highlights, dialogue options). This is enforced by the plugin itself on import as well, but
  a submission containing one will be rejected outright rather than edited.
- **Reasonable size**: routes are capped at 1500 steps; names and notes have their own length
  limits. A route that's testing those limits is probably doing too much in one file — consider
  splitting it.
- **Accurate, honest content.** A route's name and description should describe what it actually
  does. Misleading submissions will be declined.
- **The icon** must be a real, valid 48×48 PNG under 20 KB. Anything else falls back to a
  placeholder for every user, so it's worth getting right before opening the PR.

## index.json entry format

```json
{
  "id": "your-route-id",
  "name": "Your Route's Display Name",
  "author": "YourRSN",
  "description": "One sentence describing the route, under 120 characters.",
  "icon": "icons/your-route-id.png",
  "file": "routes/your-route-id.json",
  "steps": 12,
  "tags": ["questing", "early-game"],
  "updated": "2026-07-12"
}
```

`id` should be short, lowercase, and use hyphens — it becomes part of two filenames, so keep it
simple and unique. `steps` should match the actual number of steps in your route file. `updated`
is the date of your submission (or your most recent update to it), in `YYYY-MM-DD` format.

## Questions

Open an issue on this repo, or reach out via the [Route Planner plugin's GitHub](https://github.com/BlackDeath-Osrs/route-planner).
