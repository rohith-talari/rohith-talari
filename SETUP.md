# Rohith's Advanced GitHub Profile Kit

This kit is tailored to the supplied GitHub Profile Setup Guide and GitHub Profile Master Prompt.

## Files

- `README.md` — profile README. The stats cards are intentionally waiting for your Vercel deployment URL.
- `.github/workflows/snake.yml` — scheduled contribution-snake workflow.
- `assets/banner-notes.md` — banner specifications for the custom dark/light SVGs.

## Step 1 — Create the profile repository

1. Open https://github.com/new
2. Create a **public** repository named exactly `rohith-talari`.
3. Initialize it with a README if GitHub offers that option.
4. Upload the contents of this kit to the repository root, preserving `.github/workflows/snake.yml`.

## Step 2 — Finish the banner

The README expects `dark.svg` and `light.svg` in the repository root. The PDFs specify a photo-based, dithered portrait with an animated logo morph. No portrait was included with this request, so those personalized SVGs are not generated in this kit yet.

Use a clear, evenly lit, head-and-shoulders photo with a simple background. Follow `assets/banner-notes.md` to build the matching theme-aware SVGs. Do not use someone else's portrait.

## Step 3 — Configure the contribution snake

1. In **this repository's Settings** (not account settings), open **Actions → General**.
2. Under Workflow permissions, select **Read and write permissions** and save.
3. Open **Actions → Generate Snake Animation → Run workflow**.
4. Wait for the workflow to finish successfully. It should create an `output` branch.
5. Only after the first successful run, the snake image in the README should appear.

The workflow is scheduled every 12 hours, runs manually, and runs on pushes to `main`.

## Step 4 — Self-host GitHub Readme Stats on Vercel

Follow the PDF's self-hosting approach:

1. In GitHub, open Settings → Developer settings → Personal access tokens → Tokens (classic) and generate a token with the `repo` scope.
2. Copy it immediately and keep it private. Never put it in this repository, a README, a chat, or a public website.
3. Fork https://github.com/anuraghazra/github-readme-stats
4. Import your fork into https://vercel.com using the free Hobby plan.
5. In Vercel project Environment Variables, add `PAT_1` with the token as its value, then deploy.
6. Test the deployment by opening `https://YOUR-VERCEL-INSTANCE.vercel.app/api?username=rohith-talari&show_icons=true`.
7. Replace both occurrences of `YOUR-VERCEL-INSTANCE` in `README.md` with your actual Vercel deployment hostname.

Security note: the PDF suggests a classic token with no expiration, but a long-lived token increases risk. Prefer the shortest practical expiration and minimum required permissions supported by your setup. Never share the token.

## Step 5 — Verify the profile

- Confirm `dark.svg` and `light.svg` exist at the repository root before relying on the banner.
- Check the latest Actions run is green before expecting the snake to render.
- Replace `YOUR-VERCEL-INSTANCE` in both stats URLs.
- Switch GitHub appearance between dark and light to test theme swapping.
- If an image looks stale, open its raw URL with a cache-busting query such as `?v=2` and confirm the source file first.

## Known intentional omissions

- Instagram badge: no verified Instagram URL/handle was provided.
- Portfolio badge: no portfolio URL was provided.
- No fake follower counts, rankings, awards, or project links are included.
