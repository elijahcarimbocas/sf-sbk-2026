# SF SBK Congress 2026 - Road to Burlingame

One-page site for the San Francisco Salsa Bachata Kizomba Zouk Congress, Nov 19-23, 2026, Hyatt Regency San Francisco Airport.

Covers what the congress is, what the trip costs (three scenarios, every line tagged KNOWN or EST), where Burlingame actually sits relative to SFO and the city, the five-day shape, and an eight-week training arc. Live countdown to the Thursday pre-party.

Built on the same skeleton as the Hawaii 2026 site. Single self-contained `index.html`, no build step. Fonts and Leaflet load from CDN.

## Numbers are estimates

Two inputs are still missing and both need a real browser:

- **Pass tiers** sit behind the Danceplace cart (listing 15818), which asks for a login before it renders a price.
- **The Hyatt group rate** sits behind block code G-SF22. Hyatt blocks non-browser requests.

Full reasoning and sources live in `../Estimates.md`. Update the ledger in `index.html` once those two land.

## Deploy to GitHub Pages

```bash
cd "path/to/site"
git add index.html README.md
git commit -m "SF SBK Congress 2026 site"
gh repo create sf-sbk-2026 --public --source=. --push
```

Then Settings > Pages > Source = `main` branch, `/root`. Live at
`https://elijahcarimbocas.github.io/sf-sbk-2026/`

## Edit

Everything is inline in `index.html`. The cost ledger is the `.led` block in the `#bill` section. The training weeks are `.wk` blocks in `#arc`. The countdown target is one line at the top of the script.
