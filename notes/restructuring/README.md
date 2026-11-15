# Restructuring the CITF email analysis

Plan for restructuring the CITF email analysis, following the call with David and Ian on 13 November 2026. Sections:

- Preparing the corpus
- Coding rhetoric, functions and actions
- Relating rhetoric, functions and actions
- Data model and views
- Repository layout
- Next steps, up to the CIHR Project Grant application in March 2027

## Files

- `index.qmd`: the plan
- `_call-summary.qmd`: Appendix B, summary of the call
- `_transcript.qmd`: Appendix C, Grain transcript of the call
- `.gitignore`: excludes `_call-summary.qmd` and `_transcript.qmd`
- `figures/`: SVG figures used in `index.qmd`

`_call-summary.qmd` and `_transcript.qmd` are personal records of the call, so these are untracked and unrendered.

## Rendering

Run from the root of `citf-emails`. `index.qmd` includes Appendices B and C only when a render sets `call-appendices` to true.

Without Appendices B and C:

```
quarto render notes/restructuring/index.qmd
```

With Appendices B and C:

```
quarto render notes/restructuring/index.qmd -M call-appendices:true
```

Both write to the site's output folder. Render without `-M call-appendices:true` before publishing.

PDF output needs `rsvg-convert` for the SVG figures (`brew install librsvg` on macOS).
