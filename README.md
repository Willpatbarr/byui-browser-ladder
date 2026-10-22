# byui-browser ladder

Static test pages for [byui-browser](https://github.com/byui-browser), one per complexity level. Point the browser at a level's URL: a large **SUCCESS** means it passes. The browser is complete when every level passes.

| Level | Tests | Path |
|-------|-------|------|
| L0 | Plain text, no tags | `/l0/` |
| L1 | Static HTML, default styling | `/l1/` |
| L2 | Inline and `<style>` CSS | `/l2/` |
| L3 | Linked stylesheet, image, web font | `/l3/` |
| L4 | Link navigation, form submit, back/forward | `/l4/` |
| L5 | JavaScript changing the DOM | `/l5/` |
| L6 | `fetch` and `setTimeout` | `/l6/` |
| L7 | Real-world sites (linked out, checked by hand) | `/l7/` |

## Success rule

- L0/L1 just say SUCCESS: if it renders, it passes.
- L2+ show FAIL by default. Only the feature under test hides FAIL and reveals SUCCESS, so a browser without the feature shows FAIL, never a false SUCCESS.
- Each page has a short note on what it tests and what a pass looks like.

Known limits: the L3 web font and L4 back/forward are checked by eye (the page says what to look for). L0 is served as `.html` by GitHub Pages, so it contains no tags.

## Future work

- A separate ✅/❌ line per check within a level
- `console.log` success output once devtools lands
- Pass pings to a server or dashboard, and email sign-up (need a backend)
- More levels from the project lead

No build step: plain static files served by GitHub Pages.

The L3 font is Lobster (SIL Open Font License), from @fontsource/lobster.
