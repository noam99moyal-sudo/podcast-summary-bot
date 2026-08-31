# Podcast Summary Bot

Both a [Grok Bot](https://x.ai) template and a Claude skill that turn a podcast or interview into five reusable insights, plus short notes you can actually use.

You send a YouTube, X, or Spotify link. You get the argument, the claims that change what you do, and the best example from the episode.

## How to install

### Grok Bot

To add this as a Grok Bot, open the public template and import it:

**[Add Podcast Summary Bot](https://x.ai/bot/CsyAhw5YQaVLeMSnMYwgA)**

That is the install. The bot lives as a Grok Bot template, not as a GitHub app.

Template page: https://x.ai/bot/CsyAhw5YQaVLeMSnMYwgA

### Claude (claude.ai or the Claude desktop app)

**Step 1: Download the file**

👉 [Click here to download `podcast-summary.skill`](https://github.com/noam99moyal-sudo/podcast-summary-bot/releases/latest/download/podcast-summary.skill)

**Step 2: Add it to Claude**

1. Open Claude and go to **Settings**
2. Click **Capabilities**, then **Skills**
3. Click the **+** button, then **Create skill**
4. Click **Upload a skill**
5. Choose the `podcast-summary.skill` file you downloaded in Step 1

That's it. Now paste a YouTube, X, or Spotify link into Claude and ask it to summarize the episode.

### Claude Code

Open a Claude Code chat and paste in these two lines:

```
/plugin marketplace add noam99moyal-sudo/podcast-summary-bot
/plugin install podcast-summary@podcast-summary-bot
```

Then paste a link and ask, same as above.

## What you get from an episode

1. **Header** — show, episode title, host/guest, date, runtime, original link.
2. **TLDR** — exactly five bullets. Each one is a standalone insight: a model, a rule, a mechanism, a number, or a decision test. Ranked by how much it would change what a reader does, not by speaking order. Business and psychology are two example fields, not a limit on which shows it covers.
3. **Deeper notes** — one block per insight: restatement, why it holds, the strongest concrete example from the episode, and when it would fail.
4. **Worth quoting** — only if a line *is* the insight. At most one or two. Skipped if nothing is sharp.

## How insights are ranked

In this order:

1. Would this change what someone does this month, or is it just interesting?
2. Does it still stand if you never heard the episode?
3. Is there a sharp example, or only a slogan?
4. Is it the episode's actual contribution, or a famous idea that was only name-checked?
5. If two insights are true, keep the one more costly to get wrong.

## Notion is optional

The live template writes the summary in chat first.

If the person who imported it already has a Notion connector and a recaps database, it can also save a Podcast row (title, guest, show, date, runtime, source URL, tags) and apply a podcast layout if one exists.

If Notion is not connected, nothing is saved there. Importers do not need to add a Notion connector for the bot to work.

## What is in this repo

| Path | What it is |
| --- | --- |
| [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json) | Marketplace catalog — what makes `/plugin marketplace add` work |
| [`plugins/podcast-summary/.claude-plugin/plugin.json`](plugins/podcast-summary/.claude-plugin/plugin.json) | Plugin manifest |
| [`plugins/podcast-summary/skills/podcast-insight-summary/SKILL.md`](plugins/podcast-summary/skills/podcast-insight-summary/SKILL.md) | The skill: format, ranking rules, sources, optional Notion save |
| [`LICENSE`](LICENSE) | MIT |

The `podcast-summary.skill` file attached to the [latest release](https://github.com/noam99moyal-sudo/podcast-summary-bot/releases/latest) is `plugins/podcast-summary/skills/podcast-insight-summary/` pre-zipped and renamed — that's the exact file claude.ai's uploader expects (a `.skill` file, not a plain `.zip`, and not the raw folder or a loose `SKILL.md`).

No private Notion IDs, no episode content, and no API keys live here.

## License

MIT. See [LICENSE](LICENSE).
