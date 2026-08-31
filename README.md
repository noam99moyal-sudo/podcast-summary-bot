# Podcast Summary Bot

A [Grok Bot](https://x.ai) template that turns a podcast or interview into five reusable insights, plus short notes you can actually use.

It is built for business and psychology shows. You send a YouTube, X, or Spotify link. You get the argument, the claims that change what you do, and the best example from the episode. You do not get a recap of who said what in what order.

## Add it in Grok Bot (this is how people install it)

**[Add Podcast Summary Bot](https://x.ai/bot/CsyAhw5YQaVLeMSnMYwgA)**

That public template is the installable copy. Cloning this GitHub repo does not add the bot to Grok Bot. Use this repo to read the skill, fork it, or reuse the format in your own assistant.

Template page: https://x.ai/bot/CsyAhw5YQaVLeMSnMYwgA

## What you get from an episode

1. **Header** — show, episode title, host/guest, date, runtime, original link.
2. **TLDR** — exactly five bullets. Each one is a standalone insight: a model, a rule, a mechanism, a number, or a decision test. Ranked by how much it would change what a general business/psychology reader does, not by speaking order.
3. **Deeper notes** — one block per insight: restatement, why it holds, the strongest concrete example from the episode, and when it would fail.
4. **Worth quoting** — only if a line *is* the insight. At most one or two. Skipped if nothing is sharp.

## How insights are ranked

In this order:

1. Would this change what someone does this month, or is it just interesting?
2. Does it still stand if you never heard the episode?
3. Is there a sharp example, or only a slogan?
4. Is it the episode’s actual contribution, or a famous idea that was only name-checked?
5. If two insights are true, keep the one more costly to get wrong.

## Notion is optional

The live template writes the summary in chat first.

If the person who imported it already has a Notion connector and a recaps database, it can also save a Podcast row (title, guest, show, date, runtime, source URL, tags) and apply a podcast layout if one exists.

If Notion is not connected, nothing is saved there. Importers do not need to add a Notion connector for the bot to work.

## What is in this repo

| Path | What it is |
| --- | --- |
| [`skills/podcast-insight-summary/SKILL.md`](skills/podcast-insight-summary/SKILL.md) | The public skill: format, ranking rules, sources, optional Notion save |
| [`LICENSE`](LICENSE) | MIT |

No private Notion IDs, no episode content, and no API keys live here.

## Use it without Grok Bot

Copy `skills/podcast-insight-summary/SKILL.md` into any assistant that can fetch a transcript or captions from YouTube, X, or Spotify. The skill is the whole recipe. Do not invent quotes, names, numbers, or examples the episode did not contain.

## License

MIT. See [LICENSE](LICENSE).
