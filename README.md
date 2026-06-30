# sio-omb-event

Public site for the Scripps Institution of Oceanography community response to the OMB Federal Financial Assistance Rule (docket OMB-2026-0034). Comment deadline: **July 13, 2026.**

Live at: https://siodata.github.io/sio-omb-event/

## What this is

Five plain HTML pages that share one design and a sticky tab bar at the top, so a reader can move between them with one tap:

- **`index.html`** — The hub. A recap of the June 17 writing party, the live call to file a comment before July 13, the provisions you can cite, how to contact Congress, and the resource list. This is the default landing page.
- **`examples.html`** — Examples. What the community has learned about writing a comment that counts, a featured worked example, and shared templates and guidance. This page grows over time.
- **`briefing.html`** — The briefing, "The Symmetry Test." The rigorous version: ten sections, a sourced figure, four evidence-anchored scenarios, a note for counsel, a recommendation, and a three-minute floor statement for a member of Congress.
- **`oped.html`** — The op-ed, "This Isn't the Flex You Think It Is." A shorter, plain-language take built to share.
- **`news.html`** — News. A running list of the major news coverage of the OMB rule, newest first.

The tab bar appears on all five pages, in the order Hub, Examples, The briefing, The op-ed, News. The hub is the default; the others are one tap away, and each page also links to the rest from its footer.

## Structure

```
sio-omb-event/
  index.html       the hub (default landing page)
  examples.html    examples and templates
  briefing.html    the briefing
  oped.html        the op-ed
  news.html        news coverage
  README.md        this file
```

There is no build step, no framework, and no dependencies to install. Each page is a single self-contained file. Fonts load from Google Fonts; everything else (including the Scripps Pier logo on the hub and the capacity figure on the briefing and op-ed) is embedded directly in the HTML, so the files above are the entire site.

## Hosting (GitHub Pages)

See the step-by-step in the handoff notes. In short: put these files in the root of the `sio-omb-event` repository on the `main` branch, enable GitHub Pages from `main` / `/ (root)`, and the site serves at https://siodata.github.io/sio-omb-event/. The tab links are relative, so the five-tab navigation works the same locally and on Pages.

## Source

Draws on the SIO continuity and strategy document, "Scripps and the Moment." Prepared by S.C.D.
