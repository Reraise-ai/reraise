# Reraise

**The model is replaceable. Your world is not.**

Reraise is an open project by Caprey SAS, Argentina. Website: [reraise.ai](https://reraise.ai/). This repository is the home of the open card format and the project documents.

## What it is

Reraise is a layer of your own between you and any AI model. What you know lies on cards, each with its source. You and your agents read a situation on one board. And people trade cards with each other.

Your cards form a world: everything that matters to you in one context. The world stays outside the model. Claude today, another model tomorrow, a local model or your own agents can all work on the same world. An agent asks which cards are relevant to a situation and gets them, with their sources. Decisions and their outcomes become cards too.

There is no central truth and there are no editors. What counts as real in your world is up to you.

A 90-second film is on [reraise.ai](https://reraise.ai/). The whole idea in twenty short chapters: [reraise.ai/film/](https://reraise.ai/film/).

## The card

One statement, with where it comes from. A card keeps three things apart:

- **Proven**: it traces back to a source or an original. In the file: `layer: evidenced`.
- **Said**: somebody claimed it. In the file: `layer: said`.
- **Believed**: you think it is right. This is your own stance. It is not a layer and not part of the card file; it is stored apart on your device and never leaves it.

There is a third layer for things you lived through yourself: `layer: experience`. Every proven or said card needs a source.

A card is one Markdown file with YAML front matter. This is one of the citation cards on reraise.ai, complete:

```markdown
---
format: 2
id: 01M4PVTFG6418BRS9J7B2AMQ86
type: claim
title: "Many copies are not many confirmations"
language: en
layer: said
source: "Reraise film, chapter 17"
sourceDate: 2026-10-11
author: human
status: checked
worlds: [Reraise homepage]
visibility: public
release: community
training: false
edges: [01M4PVTFG4TPWE0ZWVNTERQ0KF|supports|human]
---

Ten thousand people sharing the same news wire story are not ten thousand independent confirmations. Every card keeps its origin, so copies are counted back to their source.

This is our own statement. Check it against any story you saw repeated last week.
```

`author` says who made the card: `human` or `agent:<name>`. Each entry in `edges` is `target|kind|by`: the card it points to, the kind of connection, and who drew it. The full specification is in [docs/card-format.md](docs/card-format.md). A plain introduction is at [reraise.ai/cards/](https://reraise.ai/cards/).

## The board

Cards alone are a pile. On the board they become a situation: who the players are, what drives them, what was known when. You set a guiding question, put cards on the table and seat the players.

You and your agents sit at the same board. Agents are full players: they lay cards, make cards and draw connections, and every card and connection shows who made it. Only you mark what you believe. By design, you will also mark what you think each player believes.

A clickable demo is at [reraise.ai/board/](https://reraise.ai/board/). It runs on example data: a gold market, a vitamin D claim and a Hormuz situation map. More at [reraise.ai/board-and-fields/](https://reraise.ai/board-and-fields/).

## The trade

Nobody can search the whole sky alone. So people bring in what is publicly findable, with its source, and take what they need. A first exchange is in beta at [reraise.ai/trade/](https://reraise.ai/trade/).

These rules are enforced on the exchange today:

1. Reading and taking cards is free.
2. Bringing in a card needs a number.
3. A PROVEN or SAID card needs a source.
4. At most 30 cards per member and day.
5. The origin stays on every card. Ten thousand copies of one wire story count as one source.
6. Your beliefs never leave your browser.

Standing comes first: points for origin and proof, never for volume. The full rules: [reraise.ai/trading-rules/](https://reraise.ai/trading-rules/).

## Embed a card in any web page

A quote on your page can link to its card. Put the marker right after the sentence and load the script once:

```html
Your sentence<a data-reraise-card="CARD_ID"></a>.
<script src="https://reraise.ai/embed.js" async></script>
```

Replace `CARD_ID` with the id of a card on the exchange. A demo is at [reraise.ai/embed-demo/](https://reraise.ai/embed-demo/).

## What is in this repository today, and what is not

| In this repository | |
| --- | --- |
| [docs/card-format.md](docs/card-format.md) | The card format v2 specification |
| [LICENSING.md](LICENSING.md) | Which licence applies to which part |
| [SECURITY.md](SECURITY.md) | The privacy model and how to report a vulnerability |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to take part |

The app (board, API and MCP server, the open standard through which an AI agent uses tools) works on a developer machine with an example world. Its code is not published yet and is not in this repository. The JSON Schemas that make the card format machine-readable belong to that code and are not here yet either.

Some identifiers in the card format still carry the earlier working name of the project, for example the `wb:` prefix of card URIs and the `.worldbuilder/` folder for private stances. They are part of the stored format and stay as they are.

## How to take part

- **Get your number.** Every trading partner gets a running number: [reraise.ai/#number](https://reraise.ai/#number) or [reraise.ai/trade/](https://reraise.ai/trade/).
- **Bring in a card.** One thing you found, with its source behind it.
- **Bring your field.** You know a subject better than we do. Tell us which on [reraise.ai](https://reraise.ai/#join).
- **Improve the format or the documents.** Open an issue or a discussion here.

Details in [CONTRIBUTING.md](CONTRIBUTING.md).

## Licences

- Card format, schemas, libraries, adapters and the documents in this repository: Apache License 2.0 ([LICENSE](LICENSE)).
- The app (board, API, MCP server): GNU AGPL 3.0 or later.
- The exchange platform operated by Caprey SAS is not open source.

The tool and the card format are open source and free to use. See [LICENSING.md](LICENSING.md).

## Who runs it

Reraise is an open project by Caprey SAS, Argentina.

Powered by [Private Executive](https://private-executive.com.ar)
