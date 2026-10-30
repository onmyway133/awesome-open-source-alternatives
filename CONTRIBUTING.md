# Contributing

Thanks for helping people find open source alternatives to proprietary software. Every project is
one JSON file. Open a pull request that adds or edits a file in `apps/`. A check validates it, a
maintainer reviews it, and once it's merged the project shows up in the README and on
[indiegoodies.com](https://indiegoodies.com/awesome-open-source-alternatives).

Not comfortable editing JSON? [Suggest a project with the form](../../issues/new/choose) instead.

## What belongs here

- **A real alternative** to a named proprietary product (Figma, Notion, Firebase...), usable by
  itself: an app, a self-hosted service or a platform. No libraries or SDKs.
- **Open source**, with its code on GitHub.
- **At least 1,000 GitHub stars**. The check enforces this.
- **Maintained**: not archived on GitHub.

## Add a project

Create `apps/<slug>.json`. The slug is the project's name in lowercase words joined by hyphens
(`penpot`, `uptime-kuma`). Search `apps/` first to make sure it isn't already listed.

```json
{
  "name": "Penpot",
  "repo": "penpot/penpot",
  "description": "Design and prototyping platform for teams",
  "category": "design",
  "alternativeTo": ["Figma"],
  "homepage": "https://penpot.app",
  "icon": "https://penpot.app/icon.png"
}
```

| Field | |
|---|---|
| `name` | Required. The project's name as its authors write it. |
| `repo` | Required. The GitHub repository as `owner/name`. |
| `description` | Required. One line, up to 160 characters, no trailing period. |
| `category` | Required. One slug from the table below. |
| `alternativeTo` | Required. 1 to 5 proprietary products it replaces, best known first. |
| `homepage` | Optional. The project's website, if it has one besides GitHub. |
| `icon` | Optional. A direct link to a square logo (PNG or SVG). |
| `screenshot` | Optional. A direct link to a screenshot. |
| `stars` | Leave it out. A workflow fills it in and updates it every week. |

Use 2-space indent, the key order shown above, and a trailing newline. Don't edit `README.md`: it
is generated from the JSON files after your pull request is merged.

### Categories

| Slug | Name |
|---|---|
| `backend` | Backend & Infrastructure |
| `developer-tools` | Developer Tools |
| `ai` | AI & LLMs |
| `search-data` | Search & Data |
| `analytics` | Analytics & Monitoring |
| `communication` | Communication |
| `productivity` | Productivity & Notes |
| `media` | Files & Media |
| `marketing` | Marketing & Social |
| `business` | Business & E-Commerce |
| `design` | Design |
| `security` | Security & Privacy |
| `documents` | Docs & Knowledge |
| `automation` | Automation & Scraping |
| `infrastructure` | Infrastructure as Code |
| `other` | More |

To propose a new category, open an issue first.

## Check locally

With Node 24:

```
npm ci
npm run validate
```

To also check stars, set a GitHub token: `GITHUB_TOKEN=$(gh auth token) npm run validate`.

## Pull requests

- One project (or one fix) per pull request.
- Fill in the pull request template.
