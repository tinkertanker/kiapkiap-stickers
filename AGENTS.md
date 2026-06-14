# AGENTS.md

## Identity

This repository stores Kiap Kiap sticker assets for Claw Camp. Work here is limited to producing, naming, documenting, verifying, and publishing transparent PNG sticker files. Do not add slide decks, source prompts, flattened image exports, checkerboard previews, or unrelated camp materials to this repo.

## Sticker Style

- Kiap Kiap is a cute chibi lobster mascot with a large rounded head, small compact body, tiny visible feet when the body is shown, short rounded claws, and black sunglasses.
- Use bright coral red for the lobster body, bold clean sticker outlines, and small turquoise/yellow tech accents.
- Full-body Kiap Kiap usually has a tiny smartwatch and a small mobile phone on a lanyard.
- Keep gadgets simple and readable at small sticker size. Prefer one clear prop or action per sticker.
- When Kiap Kiap is using a screen, angle the device toward Kiap Kiap unless the sticker concept specifically needs the viewer to inspect the screen. Prefer side, three-quarter, or back-facing poses over flat front-facing screens.
- VS Code stickers should read as a VS Code-like editor through dark panels, a blue sidebar, and abstract coloured code lines, but must not use the official VS Code logo or readable code text.
- Do not use existing logo marks, app logos, readable brand marks, letters, or text inside generated stickers.
- Face-only stickers should keep the oversized head, sunglasses, antennae, and friendly expression, with no body unless explicitly requested.

## File Rules

- Put final assets in `stickers/`.
- Use descriptive kebab-case filenames beginning with `kiap-kiap-`, for example `kiap-kiap-vibe-coding-game-build.png`.
- Save only final transparent PNGs in the repo.
- Do not commit generated-image IDs, flattened PNGs, checkerboard previews, temporary masks, or source scratch folders.
- Keep `.DS_Store` and other OS metadata ignored.

## Generation Workflow

1. Generate one sticker at a time so filenames can map cleanly to prompts.
2. Preserve the original generated image outside the repo when possible.
3. Copy or export only the intended final asset into `stickers/`.
4. If the generator returns a flattened background, convert only the outside-connected flat background to alpha. Avoid removing white or light interior details inside the mascot.
5. Update `README.md` when adding, renaming, or removing sticker files.
6. Run a verification pass before committing.

## Verification

Before committing, verify each new PNG:

- It is in `stickers/`.
- It has an alpha channel: `sips -g hasAlpha stickers/<file>.png`.
- It is square and consistent with the pack size unless there is a deliberate reason to differ.
- It has no text, letters, brand marks, accidental symbols, or unwanted background.
- It is visually consistent with the existing Kiap Kiap stickers.

## Git

- Keep commits atomic and stage paths explicitly.
- Use Conventional Commit messages, for example `feat: add face-only Kiap Kiap sticker`.
- Push `main` after successful verification when the user asks to publish or update the GitHub repo.
