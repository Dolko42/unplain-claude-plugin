# Unplain for Claude

Make a lead magnet with Claude and publish it with Unplain. Bring your own words, a blog post, a document or a finished PDF, or write a draft together with Claude. Unplain designs it into a branded PDF automatically, publishes it on your Library with an email form, sends the PDF to everyone who signs up, and shows you how it performs.

This plugin bundles the [Unplain connector](https://unplain.io/mcp/claude) with skills that teach Claude the whole workflow, so you can ask in plain words: "turn my last blog post into a lead magnet", "use my website's colours", "update the pricing chapter and refresh the live PDF", or "how did my guides do this month?".

Claude writes when you ask it to. Unplain never writes or rewrites your content: it designs, publishes, delivers and tracks it.

## What's inside

| Part | What it does |
|---|---|
| Unplain connector (`.mcp.json`) | Connects Claude to your Unplain account at `https://app.unplain.io/api/mcp`. You sign in with your Unplain account; no API key is stored in the plugin. |
| `create-lead-magnet` skill | From content, a web page, a PDF or just a topic to a designed ebook and a private lead magnet draft, ready to publish. |
| `set-up-brand` skill | Reads your website's name, colours, fonts and logo into a Brand Theme, or edits one by hand, and asks before public pages change. |
| `update-lead-magnet` skill | Edits a guide, refreshes the PDF of a live lead magnet, changes its landing page, pauses it, or edits your Library. |
| `lead-magnet-report` skill | Reports visitors, signups and conversion from your real numbers, finds where people drop off, and suggests next steps. |

## Getting started

1. Add the plugin, then connect Unplain from the plugin's Connectors tab and sign in. You need an Unplain account; the free plan works. Plans and limits: [unplain.io/pricing](https://unplain.io/pricing).
2. When you connect, you choose what Claude may do. Access to individual leads (emails and names) is off unless you tick it.
3. Ask Claude for a lead magnet. In Claude Code the skills are also available as `/unplain:create-lead-magnet`, `/unplain:set-up-brand`, `/unplain:update-lead-magnet` and `/unplain:lead-magnet-report`.

## Safety and what changes in public

- Nothing goes public without you. Claude creates lead magnets as private drafts and publishes only when you ask.
- Changes to anything already public (a live lead magnet, its PDF, your Library, your default brand) are shown to you first and applied only after you agree.
- Unpublishing never deletes anything: the ebook, PDF, leads and numbers are kept.
- Text from web pages, uploaded files and anything visitors typed is treated as material, never as instructions.

## Data and privacy

The plugin contains only Markdown skills and a connector address. It runs no local code, scripts or hooks, and collects nothing itself.

Everything goes through the Unplain connector to Unplain's servers at `app.unplain.io`: the content you ask Claude to turn into an ebook, brand details, lead magnet settings, and requests for performance numbers. When you use them, Unplain fetches the public web pages, PDFs and pictures you point it to. Lead data is only shared with Claude if you allowed it when connecting. How Unplain handles your data, retention and your rights: [unplain.io/privacy](https://unplain.io/privacy).

## Support

- Documentation: [unplain.io/mcp/claude](https://unplain.io/mcp/claude)
- Contact: info@unplain.io

## License

MIT, see [LICENSE](LICENSE).
