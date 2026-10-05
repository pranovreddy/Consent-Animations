# Agent Loaders — handoff

`agent-loaders.html` is a single self-contained page. Open it directly, or add `?test` to keep runs going in a hidden tab.

## v34: Hero kit (Encryption style applied to every loader)
The CSS block at the end of `<style>` ("v34 — Hero kit") and the `hero*` helpers next to `core()` in the engine script.

- **Hero**: `core()` now renders a glossy, layered squircle puck by default. It has a back plate, a gradient body, cipher dots, a top gloss, a bevel and a sweeping sheen. The agent blob sits inside it in white (`on-dark`). Its colour follows `data-state`: blue while working, amber while waiting, green when done.
  - `core(x, y, s, id, inline, { bare: true })` gives the agent alone, for scenes that build their own hero (Encryption's shield).
  - `{ orbit: false }` drops the ring in tight layouts.
- **Orbit**: a tilted ring split into back and front halves so it reads as 3D. A glint travels round it, faster in the `tool` state, and fades out when done.
- **Floor**: a lit pad under the hero with slow ripples and a contact shadow.
- **Burst**: a ring of light rays that plays once when the work seals.
- **Glass**: icon tiles (`.nd`) have a specular top and a contact shadow. Glossy icon chips have a top highlight. The stage has a key light and a vignette.
- **Encryption extras**: the shield gets an orbit ring and floor through `.hkit.back` / `.hkit.front`. The satellites' shadows breathe with their bob. Traces show marching dots flowing into the shield. On seal, the satellites, locks and ring all turn green, followed by a light burst and a ripple.
- `ctx.focus()` pads its brackets out to the hero's puck.
- Reduced motion turns off every new loop.

Timings and scene scripts are unchanged; this pass only changes the visuals.
