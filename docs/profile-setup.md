# Profile Setup Notes

## What to replace

- Replace the placeholder project links in `README.md` with the real repository URLs.
- Replace the social profile URLs if your handles change.
- Replace `assets/profile.jpg` with a real portrait or brand avatar when ready.
- Update the "What I'm Reading" section with books you are actually reading.
- Update the "My Setup" section with your actual tools and environment.
- Update the "Fun Facts" section with your own facts.

## External services used in the README

- `readme-typing-svg` for the animated headline.
- `github-readme-stats` for stats and top languages.
- `github-readme-streak-stats` for streak data.
- `github-profile-trophy` for trophy cards.
- `ghchart.rshah.org` for the contribution calendar.
- `Platane/snk` for the snake animation.
- `visitor-badge.laobi.icu` for visitor counts.
- `github-readme-activity-graph` for the activity graph.
- `skillicons.dev` for technology icon badges.

## Tokens and configuration

### Repository Secrets

- `METRICS_TOKEN` -- Fine-grained GitHub PAT with read access to public profile data (used by `metrics.yml` if `GITHUB_TOKEN` is rate-limited).
- `YOUTUBE_API_KEY` -- YouTube Data API v3 key from Google Cloud Console (used by `youtube.yml`).
- `YOUTUBE_CHANNEL_ID` -- Your YouTube channel ID, e.g. `UC...` (used by `youtube.yml`).

### Default tokens

- `GITHUB_TOKEN` -- Automatically available, used by `metrics.yml` and `snake.yml`.

## Asset layout

- `assets/banner.png` -- Wide hero banner displayed at the top of the README.
- `assets/profile.jpg` -- Avatar photo displayed in the About section.
- `svg/logo.svg` -- Brand logo (CM monogram) displayed next to the title.
- `svg/footer.svg` -- Footer wave decoration.
- `svg/wave.svg` -- Decorative wave divider between sections.
- `svg/metrics.svg` -- Workflow output from `lowlighter/metrics`.
- `svg/blog.svg` -- Static blog card.
- `svg/youtube.svg` -- Workflow output for latest YouTube videos card.

## Workflow schedule

| Workflow | Schedule | Purpose |
|----------|----------|---------|
| `snake.yml` | Daily at 00:00 UTC | Snake contribution animation |
| `blog.yml` | Manual trigger | Blog card |
| `youtube.yml` | Daily at 09:30 UTC | Latest YouTube videos card |
| `metrics.yml` | Daily at 12:00 UTC | GitHub profile metrics |

## Recommended behavior

- Keep workflow outputs committed so the README renders cleanly on first load.
- Re-run the workflows on a schedule and after relevant profile updates.
- Keep comments in the workflow files short and explicit so future edits are easy.
- Test workflows with `workflow_dispatch` before relying on the cron schedule.
