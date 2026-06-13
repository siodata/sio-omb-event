# sio-omb-event

Public site for the Scripps Institution of Oceanography response to the OMB Federal Financial Assistance Rule (docket OMB-2026-0034). Comment deadline: **July 13, 2026.**

Live at: https://sdiggs.github.io/sio-omb-event/

## What this is

Three plain HTML pages that share one design and a sticky tab bar at the top, so a reader can move between them with one tap:

- **`index.html`** — The event. The June 17 writing party at Martin Johnson House, how to file a comment that counts, the provisions you can cite, and the resource list. This is the default landing page.
- **`briefing.html`** — The briefing, "The Symmetry Test." The rigorous version: ten sections, a sourced figure, four evidence-anchored scenarios, a note for counsel, a recommendation, and a three-minute floor statement for a member of Congress.
- **`oped.html`** — The op-ed, "This Isn't the Flex You Think It Is." A shorter, plain-language take built to share.

The tab bar appears on all three pages. The event is the default; the briefing and the op-ed are one tap away, and each page also links to the other two from its footer.

## Structure

```
sio-omb-event/
  index.html       the event (default landing page)
  briefing.html    the briefing
  oped.html        the op-ed
  README.md        this file
```

There is no build step, no framework, and no dependencies to install. Each page is a single self-contained file. Fonts load from Google Fonts; everything else (including the Scripps Pier logo on the event page and the capacity figure on the briefing and op-ed) is embedded directly in the HTML, so the three files above are the entire site.

## Editing

Open the file and edit the HTML directly. Keep these standing rules:

- **No em-dashes or en-dashes.** Use commas, colons, or semicolons.
- **Never the word "foster."**
- Active voice, sentence case, plain verbs. Warm and inviting, but measured, not alarmist.
- **Public-safe:** no phone numbers or email addresses on any page. The only contact path is names plus "reach out to Helen, Nan, or Steve," and "contact Helen to join the Signal group."
- The shared Drive link and Steve's notes doc are intentionally public; keep them.

The live deadline counter on the event page is the only dynamic element. It counts down to `new Date(2026, 6, 13 ...)` in the `<script>` at the bottom of `index.html`. If the comment window is extended, change that date and the two "by July 13" label strings.

## Verify before publishing

Quick checks from the repo root:

```bash
# no em or en dashes anywhere
grep -rc $'\u2014\|\u2013' *.html

# no "foster"
grep -ric foster *.html

# tab links resolve to real files
grep -o 'href="[a-z]*\.html"' *.html | sort -u
```

All three HTML files should report 0 dashes and 0 "foster," and every tab link should point to `index.html`, `briefing.html`, or `oped.html`.

## Hosting (GitHub Pages)

See the step-by-step in the handoff notes. In short: put these four files in the root of the `sio-omb-event` repository on the `main` branch, enable GitHub Pages from `main` / `/ (root)`, and the site serves at https://sdiggs.github.io/sio-omb-event/. The tab links are relative, so the three-tab navigation works the same locally and on Pages.

## Source

Draws on the SIO continuity and strategy document, "Scripps and the Moment." Prepared by S.C.D.
