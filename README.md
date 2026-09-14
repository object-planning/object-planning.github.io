# O2P2 project page

A static restoration of **Reasoning About Physical Interactions with Object-Oriented Prediction and Planning**, based on the [July 1, 2022 Wayback Machine snapshot](https://web.archive.org/web/20220701133755/https://people.eecs.berkeley.edu/~janner/o2p2/).

## Run locally

From this directory:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open <http://127.0.0.1:8000/>. No build step, package installation, JavaScript runtime, or backend is required. Serve the page over HTTP so the YouTube player receives a referrer; opening `index.html` directly as a `file://` URL causes YouTube error 153 ("Video player configuration error") because it cannot provide the website referrer required by YouTube. Use the HTTP preview URL above. The iframe already uses `referrerpolicy="strict-origin-when-cross-origin"`, which allows the required origin referrer when the page is served over HTTP or HTTPS.

## GitHub Pages

The contents of this directory are ready to be the publishing root of a GitHub Pages repository. Keep `index.html`, `files/`, `iclr/`, and `.nojekyll` together. All local URLs are relative, so the page also works below a repository path such as `/o2p2/` or as a subdirectory of an existing personal website.

Source repository: [object-planning/object-planning.github.io](https://github.com/object-planning/object-planning.github.io). The site files belong at the repository root; no build step is required.

## Files

- `index.html`: restored page, including the original text, publication, authors, paper URL, and code URL.
- `files/main.css`: unmodified archived stylesheet.
- `files/local.css`: responsive video sizing, mobile readability, focus outlines, and equivalent styling for semantic HTML elements.
- `files/video-poster.jpg`: the original YouTube video's thumbnail, stored locally as a background while the external player loads.
- `iclr/bib.txt`: unmodified archived BibTeX citation.
- `.nojekyll`: lets GitHub Pages serve the files without Jekyll processing.

## Recovery notes

The page preserves the original desktop width, font stack, colors, spacing, section order, and 720 × 405 video dimensions. A minimum 16px margin on each side is retained at every viewport width, increasing to 24px in narrow mode (760px and below). Narrow screens use a fluid video and readable text without horizontal scrolling.

The original **`iclr/sawyer.mp4` download was not recovered**. The live Berkeley URL returns 404, and the archive's successful-capture index contains no copy. The broken download link has been removed. The original YouTube embed remains external and requires internet access. YouTube playback was verified in the local browser (the 55-second video advanced normally with no media error). A local thumbnail provides a background while the player loads.

The archived `font.css` references four Open Sans files that also return 404. The restoration uses the original stylesheet's system-font fallback stack, as the archived page does when those files are missing, and makes no broken font requests.

Obsolete `head.js` (which generated an `undefinedimages/favicon.ico` URL), duplicate metadata, browser-extension tooltip styles, and malformed markup were removed. A small inline block-themed favicon replaces the broken icon. The page uses a main landmark, labeled sections, and sequential headings with the original visual sizes. Original external author links are preserved; their destination sites are maintained independently.

## Validation

Verified the page at 1280px desktop and 390px mobile widths with no horizontal overflow, played the embedded YouTube video, and checked every local asset and citation link over HTTP at both `/` and `/o2p2/`. The abstract, archived stylesheet, and BibTeX were compared against the recovered originals.

## Sources

- [Original page HTML](https://web.archive.org/web/20220701133755id_/https://people.eecs.berkeley.edu/~janner/o2p2/)
- [Recovered stylesheet](https://web.archive.org/web/20221021202956id_/http://people.eecs.berkeley.edu/~janner/o2p2/files/main.css)
- [Recovered BibTeX](https://web.archive.org/web/20220519112637id_/https://people.eecs.berkeley.edu/~janner/o2p2/iclr/bib.txt)
- [Archive index of successful captures](https://web.archive.org/cdx/search/cdx?url=people.eecs.berkeley.edu%2F~janner%2Fo2p2%2F%2A&output=json&filter=statuscode%3A200&collapse=urlkey)
- [YouTube thumbnail](https://i.ytimg.com/vi/CXS7dRmA2hs/hqdefault.jpg)

The stylesheet and citation were served from the nearest available captures when requesting the supplied 2022 snapshot. Original content and assets retain their existing ownership; this restoration does not assign a new license.
