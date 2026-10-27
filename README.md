# catia-media

Shared media and style workspace for **Catia**, an AI virtual singer. Her look is Milan neon-noir industrial hyperpop, generated with a LoRA.

Agents use this repo to share approved images and video, keep that look consistent, and coordinate posts on X, TikTok, and Meta. [Buffer](https://buffer.com) schedules those posts from `raw.githubusercontent.com` links to files on `main`.

## Layout

| Path | Contents |
| --- | --- |
| `finals/stills/` | Approved, post-ready still images |
| `finals/video/` | Approved, post-ready video |
| `wip/` | Drafts for refining |
| `looks/<look>/` | Approved reference images for one look, for example `looks/glitch-widow/` |
| `lora/` | LoRA version notes only. Model weights stay out of this repo. |
| `posts/` | One plan file per post. Format is in `posts/README.md`. |
| `style/STYLE.md` | Palette, typography, watermark, AI-label rule, approved hashtags |

`finals/` and `looks/` are the approved libraries. Anything still being refined stays in `wip/` until it is approved and moved.

## File names

```
YYYY-MM-DD_platform_short-desc.ext
```

- `YYYY-MM-DD` is the post date in Eastern Time (`America/New_York`).
- `platform` is `x`, `tiktok`, or `meta`.
- `short-desc` is a few lowercase words joined by hyphens.
- `ext` is the real extension (`.png`, `.jpg`, `.webp`, `.mp4`, `.md`, and so on).

Examples:

- `finals/stills/2026-10-31_x_alley-portrait.png`
- `finals/video/2026-10-31_tiktok_alley-portrait.mp4`
- `posts/2026-10-31_meta_alley-portrait.md`

Look folders use a short slug: `looks/glitch-widow/`. A standing reference inside a look folder uses the same filename pattern, with the look slug as the description when it is the whole subject.

Paths stay URL-safe: lowercase ASCII, digits, hyphens, underscores, and dots. Spaces and other characters break raw links.

## Raw links

Buffer needs the raw file URL. Append the repo path to:

```
https://raw.githubusercontent.com/DensetsuMaiku/catia-media/main/
```

`finals/stills/2026-10-31_x_alley-portrait.png` is:

```
https://raw.githubusercontent.com/DensetsuMaiku/catia-media/main/finals/stills/2026-10-31_x_alley-portrait.png
```

The file has to be on `main` before that URL resolves. Media is stored as normal Git blobs (not Git LFS) so the raw URL returns the file bytes. Keep each file within GitHub's size limit.

## Rules

This repository is public. Anyone can read every file and every commit.

- Credentials, tokens, keys, personal data, and other private information stay out of the repo, including file names, captions, commits, and alt text.
- Unreleased projects, dates, and titles stay out of file names and out of every text file. A post date on an approved file is fine. A date or title for work that is not public is not.
- LoRA weights, checkpoints, and training-image sets stay out of the repo. `lora/` is notes only.
