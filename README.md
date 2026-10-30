# Smart Sort Pricing and Cost Laboratory

Mission 3, browser-only React + Vite application. Original venture site is not modified.

- Repository: https://github.com/ryancappello/costs-mission-3-
- Live URL: https://ryancappello.github.io/costs-mission-3-/
- Original venture: https://ryancappello.github.io/creative-website/smart-sort/

## Run

Node 22, pnpm 11.25.0. Run `pnpm install`, `pnpm dev`, `pnpm test`, `pnpm lint`, `pnpm build`.
GitHub Actions deploys dist to GitHub Pages with /costs-mission-3-/ base.

## Model

Annual USD physical-product model. Variable costs are per transaction/unit or percentages of revenue. Fixed recurring costs annualize monthly x12, quarterly x4, weekly x52, annual x1. One-time startup costs are separately reported as startup cash; only explicit straight-line depreciation enters accounting break-even. Shared variable costs apply per unit of every product; shared fixed costs allocate by units, revenue, or equal weights and are counted only once at business level. If all multi-product volumes are zero, no sales mix exists and break-even is undefined. Nonpositive combined contribution has no finite business break-even; individual loss-making products are flagged even when the mix remains profitable. Taxes, finance, capacity steps, demand elasticity, and detailed working-capital cycles are excluded.

## Research

research.json preserves the supplied Mission 1 dataset dated 2026-10-27. The linked venture Google Doc and local competitor spreadsheet/report and Phase_1_Pricing_Dashboard were reviewed. All five representative competitors are indirect manual sorters. Nonrepresentative bundles are excluded from the median. $149–$199 is an exploratory testing range only. Raspberry Pi board $15 and camera from $25, and Stripe US domestic online card 2.9% + $0.30 were checked on official pages 2026-10-30. Component feasibility, total manufacturing costs, and demand remain unverified. Other costs are explicitly estimated or illustrative.

## Persistence and exports

Working files and financial inputs persist in browser localStorage. Export/import JSON provides portable backup. Final DOCX and decision JSON require current evaluation, student explanation and explicit confirmation, plus warning acknowledgment if major risk is flagged. Model changes invalidate prior evaluation/exports. Both final exports use one immutable snapshot. Full decision JSON contains private financials; only the customerFacing object is intended for future public pricing display. No actual student decision is seeded.

`?qa=1` uses isolated QA storage and marks test confirmations as QA-only, never a student decision. Used to test the complete export flow. Do not use QA exports as a Mission 4 pricing decision.
