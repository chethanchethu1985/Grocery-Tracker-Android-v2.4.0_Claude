# Grocery Tracker Android - Development Progress

Current package: v2.4.0 (versionCode 25). Base: v2.3.1 package from the user.

## Milestones
| # | Milestone | Status |
|---|---|---|
| M1 | v2.4 base: version 2.4.0/25, fixed signing key for in-place updates, 8 s splash, stray `\n` and special symbols removed, dark black/grey theme, compact Purchase rows, tidy filter and add forms, partial purchase aids (select-all on focus, live "Pending after this purchase") | DONE (tested in headless Chromium at phone size; APK build not run here) |
| M2 | Decorative transparent images (groceries, medicines, stationery) on Available, Purchase, Medicines, Stationery pages, strength to be confirmed | PENDING (needs opacity decision) |
| M3 | New logo for icon, splash and header (same logo as the workout app) | PENDING (needs the logo file and which logo) |
| M4 | Spacing polish on remaining tabs (Expire, KPI, Data), optional bottom navigation | PENDING |
| M5 | Device test of the built APK, fixes, performance pass | PENDING |
| M6 | Signed release APK instructions | PENDING |

## Done in M1 (details)
- Removed a literal `\n` printed at the top of every screen; replaced pencil, cross and warning symbols with SVG icons or plain text; replaced dashes and curly quotes with plain characters.
- Partial purchase: Bought now field selects its value on focus (typing 4 gives 4, not 104), shows "Pending after this purchase: N unit" live. Verified in a real browser: planned 10, bought 4 -> Available 4, Purchase items keeps 6.
- Theme: near-black background, charcoal cards, muted teal accent. Compact header and tab chips; filter bars use label-over-field pairs.
- Splash hides after 8 seconds.
- Workflow copies signing/grocery-debug.keystore to ~/.android/debug.keystore before the build.

## Known issues and notes
- First install of 2.4.0 needs 2.3.1 uninstalled once (different signing key). Export a backup first.
- Logo is still the old CB logo until the new file is provided.
- Bill reading and Kannada translation for names outside the catalog still need the decision on API key vs offline.
- APK build and on-phone testing not yet done for 2.4.0.

## Next steps
1. User uploads 2.4.0 to GitHub, runs the workflow, installs and reports.
2. Answer: which logo (and upload the file), image strength.
3. Then M2 and M3.

## Resume rule
New session: read this file and continue from the first milestone not marked DONE.
