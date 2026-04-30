# Datagrid2+

<p align="center">
  <img src="readme-banner.svg" alt="Datagrid2+ banner" width="100%" />
</p>

**A Mendix Pluggable Widget that supercharges Datagrid 2.**

Sticky headers, sticky columns, smart column selector, header visibility, Excel-style cell borders, per-section text styling, and keyboard shortcuts — all configurable from Mendix Studio Pro. No custom CSS needed.

<p align="center">
  <strong>Coming to the Mendix Marketplace — May 2026</strong>
</p>

[![Mendix](https://img.shields.io/badge/Mendix-9.24%20%7C%2010.x%20%7C%2011.6+-0595DB?logo=mendix&logoColor=white)](https://mendix.com)
[![Marketplace](https://img.shields.io/badge/Marketplace-Coming%20May%202026-FF7900)](https://marketplace.mendix.com)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)](https://github.com/tapmaurer-repo/mendix-widget-datagrid2-plus-public/releases)

---

## Features

- **Sticky Header** — Column headers stay pinned while scrolling
- **Sticky First Column** — Pin the identifier column
- **Sticky Last Column** — Keep action buttons accessible
- **Eye Icon Merge** — Relocate the column selector into the last header, reclaim the 54px column
- **Hide Header** — Remove the header row for dashboard-style grids
- **Cell Borders** — Excel-style borders with a half-border technique
- **Text Styling** — Color, weight, and transform for header, first, and last column
- **Studio Pro Warnings** — Design-time conflict detection
- **Re-render Resilient** — Survives pagination, sorting, filtering, and column toggling

## Install

1. Download `Datagrid2Plus.mpk` from [Releases](https://github.com/tapmaurer-repo/mendix-widget-datagrid2-plus-public/releases)
2. Copy into your Mendix project's `widgets/` folder
3. Press **F4** in Studio Pro to synchronize
4. Place Datagrid2+ on your page, drop your Datagrid 2 inside, configure via properties

## Documentation

Visit the **[Datagrid2+ website](https://datagrid2plus.timothymaurer.nl)** for an interactive demo, full configuration reference, and FAQ.

## Compatibility

| Platform | Version |
|----------|---------|
| Mendix | 9.24.x, 10.x, 11.6+ (MTS) |
| Data Widgets | 3.7 (table), 3.8+ (CSS Grid) |
| Client | React Client |
| Dependencies | Zero |

## Roadmap

Ideas in the pipeline. Order reflects rough priority, not a release schedule.

- **Bulk action toolbar** — Sticky bar that slides in when rows are multi-selected, with configurable action buttons. Modern batch-action UX (Linear, Notion, Airtable) without rebuilding the action surface every time.
- **Row grouping with subtotals** — Group rows by an attribute (status, region, month), collapsible group headers, optional subtotal row per group. No working community widget currently covers this for DG2.
- **Aggregation footer row** — Sum, average, count, min, max per column, optionally recalculating against the filtered set. The original Data Grid had this; DG2 dropped it.
- **Column groups / multi-level headers** — Parent header spanning multiple columns (e.g. "Address" → Street / City / Zip). Sibling helper widget injects a header row into the existing CSS Grid via `display: contents` so column tracks stay aligned with the underlying DG2.
- **Expandable detail rows** — Click a chevron to reveal an inline accordion with a drop-zone snippet. Same snippet reusable inside a popup data view — one source of truth for create, edit, and inline-view flows.
- **User-pinnable columns** — Right-click on a column header → Pin left / Pin right, with multiple columns supported per side and state persisted alongside personalization. Extends the current sticky first/last with full end-user control.

## License

Apache 2.0 — see [LICENSE](LICENSE)

---

Built by [Tim Maurer](https://timothymaurer.nl) · Mendix UX Engineer at Aiden