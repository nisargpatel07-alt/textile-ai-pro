# Pitfalls that must never return

Each item needs a regression test before the related feature is called done.

1. **Revoked object URLs.** Never call URL.revokeObjectURL while any element still uses that URL. Prefer createImageBitmap so no URL is needed. Test: import an image, re-render the view, confirm the image still displays.
2. **Screen equals export.** The canvas the user sees must be the same data that is exported. Test: recolour, export, compare exported pixels with the displayed canvas.
3. **No flat recolouring.** Never snap each pixel to a flat palette colour. Shift each pixel relative to its matched palette colour in Lab so shading and texture survive. Test: two different shades of one region must map to two different output shades.
4. **No identity colourways.** Colourway rotation must never return the unchanged palette. Test: every variant index differs from the original.
5. **Source vs target palette.** Editing a target palette must not change the source palette used for matching pixels. Test: edit a target swatch, confirm matching is unchanged.
6. **Real percentages.** Percentages must be real shares that sum to about 100. Never show raw counts as percent. Test: palette shares sum to 100 plus or minus rounding.
7. **No fake status.** No "Saved" badge without saving, no storage meter without storage, no static rulers or dimensions. Test: every status element is bound to real state.
8. **No dead buttons.** Unbuilt features are disabled with the reason shown. Test: a UI test clicks every enabled button and expects an effect.
9. **Typeable inputs.** Controlled inputs must allow partial typing; validate on blur or Enter. Test: type a hex colour one character at a time.
10. **Stable list keys.** Never derive keys from editable values. Test: change a colour and confirm the row is not remounted.
11. **Heavy loops off the main thread.** Pixel loops run in Workers or yielding chunks, with progress and cancel. Test: a 4,000 px image keeps the interface responsive.
12. **Safe export.** Export refuses when there is nothing to export and verifies the file it wrote. Test: export with no image is blocked; exported files are re-read and checked.
