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

- **Mobile app**: iOS and Android apps — importing, library, Cooking Mode, Journal, Meal Plan, pinned recipes, Shopping Lists, Pantry, AI features, joining and editing shared collections, account, and (when enabled) subscriptions
- **Web**: viewing shared recipe lists, shopping lists, and collections. Prefer “View shared recipe lists on the web” or “Share recipe lists with a web link.”
- Do not say Souschef is "mobile-only" or that there is "no web version"
- Do not say “use Souschef fully on web,” “sync across web,” “web app,” “desktop app,” or “full web”
- Preferred framing: "View shared recipe lists on the web. Importing, cooking, and organizing happen in the iOS and Android apps."

## Subscription feature flag

Pricing and subscription docs are gated by `SUBSCRIPTION_ENABLED` in `snippets/flags.mdx`.

- **`false`:** Say the app is free. Hide billing pages and subscription copy. Feature badges show **Free**.
- **`true` (current):** Show Souschef Plus pricing, billing docs, import limits, and **Included in Free plan** badges.

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

Do **not** say “almost every feature is free” or “most features are available on the free plan.” Cooking and organization tools are free. Say that next to the import limit: free users can save 5 imported recipes per rolling 7 days. Existing saved recipes remain available even after you hit the limit.

Preferred Plus sentence: “Souschef Plus gives you unlimited recipe imports.” Plus does not unlock separate cooking tools.

Preferred free-tools sentence: “Cooking Mode, grocery lists, meal planning, cooking journal, collections, search, editing, and sharing are free.”

Do **not** describe a weekly calendar reset when you mean the rolling 7-day window.

Souschef does not serve ads for free or Plus users. Do not describe ads during imports, ad removal, or an ad-free import experience as a Plus benefit.

Imports from Instagram, TikTok, YouTube, and similar sources run in the background. Do not tell people they must keep the app open. Use: “Imports run in the background. You can keep browsing and Souschef will notify you when the recipe is ready.”

## Content boundaries

{/* Define what should and shouldn't be documented */}
{/* Example: Don't document internal admin features */}
