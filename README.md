# Thing-sona — Interactive prototype v0.3.7

A static, bilingual (English / 简体中文) prototype of Peng Lu’s Thing-sona tool.

## Open

Open `index.html` in a modern browser. No installation or build step is required. All card artwork is bundled locally; the app makes no network requests.

## GitHub Pages

1. Extract this ZIP.
2. Upload the **contents** of the `thing-sona` folder (`index.html`, `assets`, and the documentation) into your repository root, or a subfolder such as `Thing-sona/` in an existing Pages repository.
3. For a new Pages repository, select Settings → Pages → Deploy from a branch, and select your branch and root folder. If Pages is already configured, retain its existing setup.
4. With a subfolder, the page will be at the existing Pages URL followed by `/Thing-sona/` (case sensitive).

GitHub settings labels can vary. This package has not been pushed to a GitHub repository or deployed.

## Included interactions

- 13 original Who cards and 7 original How cards.
- Expected and experienced relations, one How + Who pair per side.
- Original card illustrations rendered from the supplied print PDF.
- Native desktop drag-and-drop from the library into any matching How / Who slot, with visual target feedback. Click selection remains available, including on touch devices.
- Custom cards with participant-authored titles, descriptions, and a curated collection of 726 bundled Noto Emoji SVG illustrations. Search in English or Chinese; filter by category; preview before saving.
- Manage cards: edit or delete custom cards in the current project. Deleting a placed card clears its slots after confirmation but preserves narratives. Original cards remain available.
- Custom card artwork is included in JSON exports by its bundled asset identifier.
- Technology, participant perspective, narratives and reflection.
- Twelve optional context prompts: activity/intention, physical/digital setting, familiarity, other people/technologies, initiation/choice, action/decision-making, frequency/duration, participant state, timing/pace, resources/constraints, social/organisational context, and other factors.
- Multiple projects in localStorage.
- JSON export/import, including custom cards and contextual records.
- Print styling for browser Print / Save as PDF.
- Responsive layouts, keyboard-operable buttons and labeled inputs.

## Research fidelity

Based on the supplied `IASDR2025 submission.pdf`, `Thing-sona.pdf`, `Thing-sona Deck_Usage.pdf` and `Thing-sona Deck_CN V1.3.pdf`.

The focus is the participant’s subjective experience of a situated human–technology relation. The prototype does not classify a technology’s autonomous personality. It is a generative and speculative tool, not a validated measurement instrument.

The Chinese card titles and descriptions follow the print deck. English titles and descriptions are provisional translations; they need author review before formal research use. The AI-assisted writing example is explicitly illustrative, not a transcript or empirical finding. Its card pairing demonstrates how the tool can be explored beyond driving. Research-history text retains the tool’s origins in co-driving.

Context prompts have been adapted across technologies and practices without claiming validation in those settings. All are optional. Existing driving-specific fields from v0.1 remain in saved/imported projects and appear under retained details when they contain values; empty legacy prompts are omitted. The original PDFs and unpublished manuscript are not redistributed in this package.

The CSS requests IBM Plex Sans, the typeface identified in the supplied usage sheet, then uses system fallbacks. No font binary is included. To make the exact font consistent across computers, add an appropriately licensed local font and an @font-face rule.

## Data

Everything stays in the browser. JSON export is the portable backup. Browser storage can be cleared, and file:// storage behavior varies between browsers; use JSON backups and preferably open from GitHub Pages for stable origin-based storage. Imported projects are added as new projects, preserving existing work. There are no accounts, analytics, cloud sync or collaborative sessions.

## Verification

JavaScript syntax and targeted logic checks passed for generalised contexts, legacy context retention, image validation and JSON roundtrips, custom card editing/deletion, used-slot cleanup with narrative preservation, matched and mismatched native drag/drop event handlers, and bilingual rendering. The local SVG assets were parsed and checked. These are logic/event-handler checks, not an actual browser drag test. Browser visual QA was unavailable in the authoring environment; desktop/mobile rendering and print pagination should receive a final browser check.

## Credits and rights

Thing-sona: Peng Lu. Original print deck marked Apache-2.0. Original illustrations credited to Noto Emoji (Google); see `NOTICE.md`. New prototype code is supplied for the author to review and publish under their chosen license. This package does not change the licensing of the supplied materials.

## Updating from v0.1

Replace the existing `index.html` and the full `assets/` folder. Keep the same published URL/browser origin to retain local projects. The localStorage key and JSON version remain compatible; v0.3 imports v0.1 files. New image choices require the v0.3 assets. Export your projects before moving to another origin or browser.

Custom cards currently belong to their project and travel with that project’s JSON. Card management explicitly displays this scope. Native drag-and-drop targets desktop browsers; touch users can continue tapping a slot and then a card.

## v0.3 interface update

- New has a red background; the blue example button reads “Show me the example”.
- Desktop card-library and relation-workspace bottom edges align; narrow screens retain stacked layout.
- Noto selection covers eight categories, with English/Chinese CLDR names and search keywords. Results display in batches of 80, with a Show more button.
- The two requested explanatory sentences have been removed from the webpage in both languages.

## v0.3.1

Opening the custom-card / emoji dialog locks background scrolling. The dialog and emoji grid contain their scroll gestures. Closing via Cancel, Save or Escape restores the original page position and inline styles.

## v0.3.2

Every page load starts in English. Switching language localises the built-in writing example, project selector, form text, card-type options and print heading. Known bilingual example values from earlier versions are migrated when displayed. Participant-authored or edited text is preserved verbatim, not automatically translated.

## v0.3.3

- The phrase “the relations” and its Chinese counterpart use the original pink-red accent; “we experience” retains blue in English.
- A red-and-blue two-dot SVG favicon and a 180 px touch icon match the header mark.
- From 701 px upward, the card grid removes its fixed 520 px cap and fills the equal-height library panel. The compact mobile scroller remains unchanged.

## v0.3.4

The relation workspace now determines the Card Library height in one direction. A ResizeObserver and window resize handler recalculate that height whenever the responsive layout changes, so resizing from a narrow single-column board back to a wide two-column board contracts the library again. At 700 px or below the explicit height is removed for the stacked mobile layout.

## v0.3.5

The card removal button now uses a dedicated 1:1 line box and flex centering so the multiplication sign is centred vertically and horizontally inside its circle.

## v0.3.6

Card Library height now follows the whole relation workspace only above 1050 px, where the two relation boards share a row. From 701–1050 px, where the relation boards stack, it follows the first board instead of the combined height of both boards and the reflection area. At 700 px or below, the explicit height is cleared.

## v0.3.7

At intermediate widths, the Card Library follows the selected relation board. Selecting Expected or Experienced moves the library alongside that board and matches its height, while preserving the current card filter and scroll position.
