# Profile Setup Notes

## What to replace

- Replace the placeholder project links in `README.md` with the real repository URLs.
- Replace the social profile URLs if your handles change.
- Replace `assets/profile.png` with a real portrait or brand avatar when ready.

## External services used in the README

- `readme-typing-svg` for the animated headline.
- `github-readme-stats` for stats and top languages.
- `github-readme-streak-stats` for streak data.
- `github-profile-trophy` for trophy cards.
- `ghchart.rshah.org` for the contribution calendar.
- `Platane/snk` for the snake animation.
- `visitor-badge.laobi.icu` for visitor counts.

## Tokens and configuration

- `metrics.yml` can run with `GITHUB_TOKEN` for public profile metrics.
- If the metrics workflow gets rate-limited, create a fine-grained GitHub token with read access to public profile data and store it as `METRICS_TOKEN`.
- `waka.yml` needs a WakaTime API key stored as `WAKATIME_API_KEY` and a GitHub token stored as `GH_TOKEN` or `GITHUB_TOKEN`.
- `youtube.yml` is scaffolded to let you plug in a YouTube Data API key if you want live channel stats later.
- `blog.yml` is scaffolded to let you wire in your RSS feed and refresh cadence.

## Asset layout

- `assets/banner.png` is the wide hero image.
- `assets/profile.png` is the avatar or monogram image.
- `svg/logo.svg` is the brand mark.
- `svg/footer.svg` is the footer wave.
- `svg/wave.svg` is the decorative wave divider.
- `svg/metrics.svg`, `svg/waka.svg`, `svg/blog.svg`, and `svg/youtube.svg` are workflow outputs.

## Recommended workflow behavior

- Keep workflow outputs committed so the README renders cleanly on first load.
- Re-run the workflows on a schedule and after relevant profile updates.
- Keep comments in the workflow files short and explicit so future edits are easy.