# BOHAM Praia — Demo site (GitHub Pages)

A private design preview for BOHAM Praia. This folder is ready to upload to a **new, separate GitHub repository** and publish for free via GitHub Pages.

---

## What's in this folder

```
boham-site/
├── index.html          ← the website (with password gate + watermark)
├── capabilities.html   ← client explainer page (CMS + integrations)
├── images/             ← drop the real photos here (see names below)
└── README.md           ← this guide
```

---

## Publish it (no terminal needed — GitHub website only)

1. **Create a GitHub account** at github.com (free) if you don't have one.
2. Click **New repository**. Name it `boham` (lowercase). Keep it **Public** — required for free GitHub Pages. Click **Create repository**.
3. On the repo page, click **Add file → Upload files**. Drag in **everything inside this `boham-site` folder** (the `index.html`, `capabilities.html`, and the `images` folder). Click **Commit changes**.
4. Go to **Settings → Pages**. Under *Build and deployment → Source*, choose **Deploy from a branch**, branch **main**, folder **/ (root)**. Click **Save**.
5. Wait ~1 minute, then your live URL appears at the top of that Pages screen:

   **https://YOUR-USERNAME.github.io/boham/**

   The client explainer is at `…/boham/capabilities.html`.

Share that URL with the client.

---

## The demo password

- The site is gated. Current password: **`BOHAM2026`**
- Share the password **separately** from the link (e.g. by message), not in the same email.
- To change it: open `index.html`, find `var PW = "BOHAM2026";` near the bottom, change the value, re-upload the file.

---

## Adding the real photos

Put your JPGs in the `images/` folder using these exact names — they slot in automatically:

| File name | Photo |
|---|---|
| `01-kite-storage.jpg` | Kite storage room / gear |
| `02-entrance.jpg` | Entrance / restaurant |
| `03-pool-people.jpg` | Pool with people |
| `04-pool-coconut.jpg` | Drinks / coconut at the pool |
| `05-deck-beach-sunset.jpg` | Beach deck at golden hour / kite |
| `06-rooftop-lounge.jpg` | Rooftop bean-bag lounge |
| `07-pool-architecture.jpg` | Architecture + pool + village |
| `08-sunset-crowd.jpg` | Sunset crowd / music (also the hero) |

Until a file exists, that slot shows a tasteful colour gradient — nothing breaks.

---

## Update the links

Open `index.html`, find the `CONFIG` block near the bottom, and fill in:

```js
const CONFIG = {
  whatsapp:    "https://wa.me/55XXXXXXXXXXX",  // confirm the number
  maps:        "https://www.google.com/maps/...",
  instagram:   "https://www.instagram.com/bohampraia/",
  menu:        "",   // paste menu / Linktree URL
  tripadvisor: "",   // paste Tripadvisor URL
  google:      ""    // paste Google reviews URL
};
```

Empty values (`""`) automatically hide that button until you add a link.

---

## Honest note on protection

GitHub Pages serves a **public, static** website, so the password gate and anti-copy measures add **friction** but are **not unbreakable** — anyone technical can still view the source. That's true of every live website.

If you need stronger gating (a real server-side password, or keeping the source out of public view), host on **Netlify** or **Vercel** instead — both are free and support password-protected previews. The real, defensible value isn't the HTML anyway: it's the **CMS, booking system, and custom integrations** that live on a private backend (see `capabilities.html`).
