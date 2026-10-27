# Post plans

One file per scheduled post. The file name matches the media it points at:

```
YYYY-MM-DD_platform_short-desc.md
```

`platform` is `x`, `tiktok`, or `meta`. A cross-post is three files, one per platform, even when the caption is shared.

## Format

```
date: YYYY-MM-DD
timezone: America/New_York
platform: x
media: finals/stills/YYYY-MM-DD_x_short-desc.png
caption: |
  Caption text.
```

| Field | Meaning |
| --- | --- |
| `date` | Post date in Eastern Time |
| `timezone` | Always `America/New_York` |
| `platform` | `x`, `tiktok`, or `meta` |
| `media` | Repo path of the approved file under `finals/` |
| `caption` | Exact caption to schedule, including hashtags |

The media file is already on `main` under `finals/` before the plan is scheduled. Buffer uses the raw link for `media`:

```
https://raw.githubusercontent.com/DensetsuMaiku/catia-media/main/<media>
```

Hashtags come from the approved list in `style/STYLE.md`. Video captions also follow the AI-label rule in that guide. Captions stay inside the public-repo rules in the root README.
