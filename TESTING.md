# Verification record

Tested October 30, 2026.

## Automated

24 Node tests pass (`pnpm test`). They independently check single-product revenue/cost/profit and break-even, upward unit rounding, zero/negative contribution, weekly/monthly/quarterly annualization, startup cash versus depreciation, nondepreciating working capital, price-sensitive percentage fees, disabled costs, multi-product shared overhead and allocations, assigned costs, zero-volume mix handling, cost-category reconciliation, stale-model fingerprints, competitor median and bundle exclusions, import guardrails, presets, stress tests, immutable snapshots, and genuine DOCX generation.

`pnpm lint` syntax checks the model, cost data, and report module. Vite production build passes and includes React JSX parsing. The DOCX library makes the initial JavaScript bundle larger than 500 kB; Vite reports a size advisory, not a build error.

## Browser production-preview QA

Used isolated `?qa=1` storage. Changed product price to $50: negative contribution and no finite break-even appeared. Added and removed a product. Moved the frame-cost slider with ArrowRight ($20 to $21), precisely edited its numeric value, toggled the expense off/on, added a custom expense, changed monthly to quarterly ($100 became $400 annually), edited its description, then deleted it. Applied Lean and Typical presets and saved a custom scenario. Confirmed reload retained the working model. Exported a working JSON, imported it through file upload, and validated restoration. Checked pricing charts and competitive context. Evaluated pricing, revised the price to $180, saw the evaluation become outdated and confirmation disabled, then reevaluated. Supplied an explicit QA-only explanation, acknowledged warnings, and created a test-only snapshot. This was not the student's pricing decision.

Browser-generated DOCX and JSON downloads saved to Downloads. ZIP integrity and OOXML were checked; all ten report sections, selected price, justification, original URLs, confirmation timestamp, and JSON financial identity matched. Rendered all 11 report pages and visually inspected each for clipping, broken tables, missing text, and spacing. The report is legible and tables repeat headers across page breaks.

Tested 390 x 844 mobile viewport: no page-wide horizontal overflow, menu opened, charts resized, and navigation worked. Restored viewport afterward. No actual student pricing decision has been confirmed. The original venture project was not edited.

## Remaining model limits

Most costs are estimated, not supplier quotations. Hardware performance, demand, capacity steps, taxes, financing and detailed working-capital cycles remain unvalidated or outside the model. Representative competitor prices are the dated Mission 1 snapshot, not live prices. The exploratory $149–$199 range is not validated willingness to pay. All such limits appear in the interface and reports.
