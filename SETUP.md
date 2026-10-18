# GitHub profile implementation — Talari Rohith

This implementation follows the two supplied PDFs' sequence and palette:
1. Special profile repository and theme-aware banner
2. Self-hosted GitHub Readme Stats on Vercel
3. Scheduled contribution snake
4. Social badges

## Repository

The special profile repository must be named exactly `rohith-talari` and belong to the GitHub account `rohith-talari`.

Upload `README.md` and the `.github/workflows/snake.yml` file to the repository root, preserving the hidden `.github` directory.

## Phase 1 — Banner assets (photo required)

The README references `dark.svg` and `light.svg` at the repository root. The supplied Master Prompt explicitly specifies a photo-derived dithered portrait and animated logo morph. No portrait photo was supplied with the request, so those final custom assets cannot be truthfully generated from your appearance yet.

Upload a clear head-and-shoulders photo with a plain background to complete this phase. Banner specification:
- SVG canvas: 1180 × 610; terminal title `profile.sh --live`
- Left ~38%: portrait frame labelled `VISUAL.MAP`
- Right: `SYSTEM.INFO` rows, dotted leaders, LIVE indicator, handle pill
- Palette: background `#0A101F`, cyan `#22D3EE`, violet `#A78BFA`, green `#10B981`
- Both `dark.svg` and `light.svg`; theme-aware `<picture>` already exists in README.

## Phase 2 — Self-host GitHub Readme Stats

1. Fork https://github.com/anuraghazra/github-readme-stats
2. Import the fork into https://vercel.com and deploy with the free Hobby plan.
3. Add an environment variable named `PAT_1` containing a GitHub token, following the upstream project's current documentation.
4. Never commit the token or share it in chat. Prefer an expiring token with the minimum permissions required rather than an unnecessarily permanent credential.
5. Replace `YOUR-VERCEL-INSTANCE` in the two README stats URLs with the Vercel deployment hostname.
6. Test: `https://YOUR-VERCEL-INSTANCE.vercel.app/api?username=rohith-talari&show_icons=true`

## Phase 3 — Contribution snake

1. Open this repository's **Settings → Actions → General**.
2. Under **Workflow permissions**, choose **Read and write permissions**, then save. This is repository settings, not account settings.
3. Open **Actions → Generate Snake Animation → Run workflow**.
4. Wait for the workflow to finish green and create the `output` branch. Only then should the snake images render.
5. The workflow runs on pushes to `main` and every 12 hours.

## Phase 4 — Social badges

LinkedIn and email badges are configured. The LinkedIn badge uses brand blue `#0A66C2` as the supplied PDF warns that custom colors can cause the logo glyph to disappear. Instagram and portfolio links are omitted because verified URLs were not supplied.

## Final verification

- Confirm the actual GitHub account owns `rohith-talari`.
- Add `dark.svg` and `light.svg` to the repository root after creating the photo-derived banner.
- Replace both `YOUR-VERCEL-INSTANCE` placeholders.
- Run the snake workflow successfully before expecting its images to appear.
- Switch GitHub appearance between dark and light to test the banner.
