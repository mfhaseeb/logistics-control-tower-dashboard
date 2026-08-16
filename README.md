# Logistics Control Tower Dashboard (Power BI)

A two-page operational dashboard built in Power BI for freight/logistics tracking — designed to answer one core question:

> **Which lanes and carriers are driving booking and delivery delays, and where in the shipment lifecycle are those delays happening?**

*Note: this repo contains a sanitized sample version. All figures, booking numbers, and client identifiers have been replaced with synthetic data — see `logistics-control-tower.html` for a static, dependency-free preview.*

## What it does

**Overview page**
- Tracks Total Bookings, Bills of Lading, and Shipments with week-over-week trend arrows
- Breaks "on-time" performance into three layers — Business (actual delivery), Planning (main carriage), and Booking — to isolate *where* in the process delays originate rather than reporting one blended number
- Shipment distribution by market (donut) and a lane-level table (carrier, count, lead time vs. actual transit time) for drill-down

**Deviation Report page**
- Row-level detail comparing planned vs. actual departure/arrival dates per booking
- Flags deviations with a simple red/green indicator, filterable by market, carrier, booking/BL number, and pull-out week
- Built for an ops team to triage specific shipments, not just monitor aggregate KPIs

## Why the three-tier on-time breakdown matters

The most interesting finding in the live version of this dashboard was a **~20-point gap between Business On Time (96.7%) and Planning On Time (76.9%)** — meaning shipments were arriving roughly on the delivery deadline, but the *planned* main-carriage schedule was being missed far more often. That gap is the kind of signal a flat "on-time %" KPI would hide, and it's the layer worth investigating first.

## Tech

- Power BI Desktop (data model, DAX measures, slicers/cross-filtering)
- `logistics-control-tower.html` — a static HTML/CSS/JS recreation of both pages for quick preview without opening Power BI

## Preview

Open `logistics-control-tower.html` in any browser, or view screenshots below.
