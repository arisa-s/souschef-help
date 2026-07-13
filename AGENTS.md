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

- **Full experience** / **mobile app**: iOS and Android apps — importing, library, Cooking Mode, Shopping Lists, Pantry, AI features, account, and subscriptions
- **Web version** / **lightweight web viewer**: browser experience for viewing shared recipe links only (view recipe, adjust servings, switch measurement systems)
- Do not say Souschef is "mobile-only" or that there is "no web version"
- Preferred framing: "Souschef has a lightweight web version for viewing shared recipes. To import recipes, organize your library, and access the full feature set, use the iOS or Android app."

## Style preferences

{/* Add any project-specific style rules below */}

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

### Feature availability badges

Almost every product feature is available on the free plan. Souschef Plus is primarily for unlimited recipe imports and an ad-free import experience.

On major feature pages, place a linked availability badge immediately below the title:

```mdx
<a href="/billing/free-plan" className="help-availability-badge">
  <Badge icon="circle-check" color="green" shape="pill">Included in Free plan</Badge>
</a>
```

For Souschef Plus pages (`subscription-benefits`, `subscribe`):

```mdx
<a href="/billing/free-plan" className="help-availability-badge">
  <Badge icon="star" color="yellow" shape="pill">Souschef Plus</Badge>
</a>
```

Do **not** label Cooking Mode, Shopping Lists, Pantry, Nutrition, AI features, printing, servings, measurement conversion, timers, organization, sharing, or import sources as Plus-only.

## Content boundaries

{/* Define what should and shouldn't be documented */}
{/* Example: Don't document internal admin features */}
