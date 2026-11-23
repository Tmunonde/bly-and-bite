# Bly & Bite

One website with two mobile apps. Each one sends orders and booking requests to WhatsApp.

| Path | App |
|---|---|
| `/` | Landing page linking to both apps |
| [`/pies/`](pies/) | **Pie orders**: shops order Johan's pies and chilli biltong ([details](pies/README.md)) |
| [`/stays/`](stays/) | **Stay booking**: find guesthouses and B&Bs and send booking requests to hosts ([details](stays/README.md)) |

Each app also has a `bot.html` demo of its WhatsApp bot, and a `bot/` folder with the real WhatsApp Cloud API bot (a Cloudflare Worker). The two bots are deployed separately, because each WhatsApp number needs its own webhook.

WhatsApp number used for now: **067 207 5483** (`27672075483`). Change it in `pies/data/catalog.js` and `stays/data/listings.js`.

## Publish (GitHub Pages)
Repo → **Settings → Pages** → *Deploy from a branch* → `main` / `(root)` → Save.

Live at `https://tmunonde.github.io/bly-and-bite/`, with the apps at `/pies/` and `/stays/`.

## Develop
```bash
npm test               # tests for both bots
npm run serve          # http://localhost:8080
npm run chat:pies      # chat with a bot in the terminal
npm run chat:stays
npm run bot:deploy:pies   # deploy a bot (see each app's README for the Meta setup)
npm run bot:deploy:stays
```

Product prices and the guesthouse listings are **demo placeholders**.
