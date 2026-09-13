# Requirements — DevPulse Narrated Walkthrough

## Purpose
A standalone, single-file HTML page that narrates a clear explanation of the DevPulse
developer productivity dashboard out loud, using the browser's built-in text-to-speech
(Web Speech API) — no audio file, no external service, no API key.

## Functional requirements
1. A "Play narration" button starts reading a 10-section script aloud, section by section.
2. Pause / Resume control mid-narration.
3. Restart control to replay from the beginning.
4. A voice picker listing the browser's available English voices.
5. The section currently being read is visually highlighted and auto-scrolled into view;
   completed sections are visually marked as done.
6. A progress bar and "Section X of Y" label track playback position.
7. Graceful fallback: if the browser doesn't support speech synthesis, the play button is
   disabled and a visible note explains the script can still be read silently on the page.
8. A direct link to the live deployed dashboard.

## Non-functional requirements
- Zero dependencies — plain HTML/CSS/JS, works as a single static file.
- Visual style matches the DevPulse dashboard's own dark theme and color tokens, so the two
  feel like one product.
- Respects `prefers-reduced-motion`.
- Deployable to GitHub Pages exactly like the rest of the project portfolio.

## Out of scope
- Recording or exporting an actual audio/video file — this page narrates live, in-browser,
  each time it's opened; it does not produce a downloadable video.
