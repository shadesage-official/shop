# shadesage-official.github.io

The ShadeSage lip shade finder — a single static page, no build step, no dependencies.

- `index.html` — the whole site (HTML + CSS + JS + product data in one file).

## Adding a shade

Open `index.html`, find the `PRODUCTS` array near the bottom of the `<script>` block, and add one object:

```js
{
  brand: "Maybelline",
  shade: "Upstate",
  product: "Serum Lipstick",
  videos: ["v1"],                                   // ids from the VIDEOS array
  url: "https://www.amazon.com/s?k=...&tag=shadesagebeau-20"
}
```

- Keep `tag=shadesagebeau-20` on every Amazon link.
- The same product found in a second video: add that video id to `videos` instead of adding a
  second object. The page shows the product once and lists every video it appeared in as a badge.
- A new video: add it to `VIDEOS` first (`id`, `title`, `short`, `youtube`, `tiktok`).

## Rules for this site

- No "dupe"/"dupes" wording anywhere on the page.
- The Amazon disclosure line stays at the bottom, fixed:
  `As an Amazon Associate I earn from qualifying purchases.`
