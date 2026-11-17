# QA — 17 November 2026

Tested locally with headless Google Chrome via Playwright. No build is required for this static HTML project.

| Check | Result |
| --- | --- |
| Responsive widths 1440, 768, 620, 390, 375, 320 px | PASS: no horizontal overflow |
| Gallery | PASS: 4 square cells in a 2×2 grid; left screenshot remains 9:16 at all tested widths |
| Images | PASS: all 8 images load at all tested widths |
| Original assets | PASS: all 5 original V7 assets are byte-identical to the source ZIP |
| Visual review | PASS: desktop 1440, tablet 768 and mobile 390 screenshots inspected |
| Navigation | PASS: My work scrolls to #work |
| External link activation | PASS: all 4 links open a new tab to their exact configured URL; target responses were intercepted for this interaction check |
| External destination HTTP requests | PASS: TikTok, Lemon8 and Instagram each returned HTTP 200; TikTok and Lemon8 resolved their share redirects |
| Phone and email | PASS: correct displayed values and tel:/mailto: destinations; native phone/mail applications were not launched |
| Resume | PASS: actual browser download, correct filename, application/pdf, HTTP 200, 195667 bytes, downloaded bytes identical to original |
| Keyboard | PASS: all 8 links reachable in document order with visible focus |
| Reduced motion | PASS: smooth scrolling disabled when requested |
| Runtime | PASS: no JavaScript page errors |
| Basic accessibility (axe WCAG A/AA scan) | Existing contrast issue: small paragraph text in cards 02 and 03 uses the original muted color on pale lavender; retained to respect the explicit requirement to preserve colors |
| Git whitespace check | PASS: git diff --check |

The accessibility scan found only the color-contrast rule on paragraphs in cards 02 and 03, at every tested width. Other scanned rules passed; this is not a claim of full accessibility conformance. Image descriptions, document language, heading structure, and link labels were included in the checks.

The photographs are the four original supplied collages, one file per gallery cell. Centered square cropping is performed by CSS and does not alter the source JPEGs. The screenshot, covers, profile and resume are preserved from V7.

Live social account content and app/login behavior are outside the HTTP/link checks. GitHub Pages has not been published as part of this preparation. The finalized changes are committed to the existing GitHub repository on main.
