# Pitfalls

These are mandatory acceptance constraints:

1. Never revoke a blob URL while it is still in use. Prefer `createImageBitmap` or retain URLs until replacement/unmount.
2. The canvas shown to the user is the canvas that exports.
3. Recolour exact work in Lab with soft source matching and lightness preservation.
4. Never generate an identity colourway.
5. Keep source palette matching independent from editable target palette values.
6. Display real percentages, never raw counts.
7. Never show invented saved, storage, document-size or ruler values.
8. Disable unbuilt features and state the reason.
9. Validate controlled text fields on blur or Enter.
10. Use stable row IDs as React keys.
11. Run heavy pixel loops in workers or bounded chunks.
12. Refuse exports with no source and re-open exported files for verification.
