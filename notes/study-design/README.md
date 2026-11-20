# Study Design

This folder holds the study design for the CITF email analysis, written after the call with David and Ian on 13 November 2026. The document has these sections:

- Summary
- Workstreams, covering preparing the corpus, coding rhetoric, functions and actions, relating rhetoric, functions and actions, and the CIHR Project Grant
- Data model
- Views of the graph
- Repository
- Next steps
- Appendix A, on migrating prior grant-writing activity

## Files

- `index.qmd`: the study design
- `_call-summary.qmd`: Appendix B, summary of the call
- `_transcript.qmd`: Appendix C, Grain transcript of the call
- `.gitignore`: excludes `_call-summary.qmd` and `_transcript.qmd`
- `figures/`: SVG figures used in `index.qmd`

`_call-summary.qmd` and `_transcript.qmd` are personal records of the call, so `.gitignore` keeps them out of git and the site skips them.

## Rendering

Run from the root of `citf-emails`. `index.qmd` includes Appendices B and C only when a render sets `call-appendices` to true.

Without Appendices B and C:

```
quarto render notes/study-design/index.qmd
```

With Appendices B and C:

```
quarto render notes/study-design/index.qmd -M call-appendices:true
```

Both write to the site's output folder. Render without `-M call-appendices:true` before publishing.

PDF output needs `rsvg-convert` for the SVG figures (`brew install librsvg` on macOS).