> **First-time setup**: Customize this file for your project. Prompt the user to customize this file for their project.
> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Use the Mintlify MCP server, `https://mcp.mintlify.com`, to edit content and settings via MCP
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, to query information about using Mintlify via MCP

## Terminology

- **Full experience** / **mobile app**: iOS and Android apps — importing, library, Cooking Mode, Journal, Meal Plan, pinned recipes, Shopping Lists, Pantry, AI features, joining and editing shared collections, account, and (when enabled) subscriptions
- **Web version** / **lightweight web viewer**: browser experience for shared recipe links (view recipe, adjust servings, switch measurement systems), shared shopping lists, and peeking at shared collections
- Do not say Souschef is "mobile-only" or that there is "no web version"
- Preferred framing: "Souschef has a lightweight web version for viewing shared recipes, shopping lists, and collections. To import recipes, organize your library, journal, plan meals, and access the full feature set, use the iOS or Android app."

## Subscription feature flag

Pricing and subscription docs are gated by `SUBSCRIPTION_ENABLED` in `snippets/flags.mdx`.

- **`false` (current):** Say the app is free. Hide billing pages and subscription copy. Feature badges show **Free**.
- **`true`:** Show Souschef Plus pricing, billing docs, import limits, and **Included in Free plan** badges.

When flipping the flag to `true`, also:

1. Restore nav from `snippets/subscription-nav.json` into `docs.json` (Billing group + `troubleshooting/subscription-not-recognized`)
2. Remove `hidden: true` and `noindex: true` from every file in `billing/` and from `troubleshooting/subscription-not-recognized.mdx`

Use shared snippets for gated copy:

- `snippets/AvailabilityBadge.mdx` — feature availability badge
- `snippets/IsSouschefFree.mdx` / `IsSouschefFreeShort.mdx` — “Is Souschef free?” answers
- Import `{ SUBSCRIPTION_ENABLED }` from `snippets/flags.mdx` for conditional blocks

## Style preferences

{/* Add any project-specific style rules below */}

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

### Feature availability badges

On major feature pages, place the availability badge immediately below the title:

```mdx
import AvailabilityBadge from "/snippets/AvailabilityBadge.mdx";

<AvailabilityBadge />
```

When `SUBSCRIPTION_ENABLED` is true, the badge links to the free plan page. When false, it shows **Free** with no billing link.

For Souschef Plus pages (`subscription-benefits`, `subscribe`) when subscriptions are enabled:

```mdx
<a href="/billing/free-plan" className="help-availability-badge">
 <Badge icon="star" color="yellow" shape="pill">Souschef Plus</Badge>
</a>
```

Do **not** label Cooking Mode, Shopping Lists, Pantry, Nutrition, AI features, printing, servings, measurement conversion, timers, organization, Journal, Meal Plan, pinned recipes, sharing, or import sources as Plus-only.

## Content boundaries

{/* Define what should and shouldn't be documented */}
{/* Example: Don't document internal admin features */}
