# Logistics Control Tower Dashboard (Power BI)

A two-page operational dashboard built in Power BI for freight/logistics tracking — designed to answer one core question:

**Which lanes and carriers are driving booking and delivery delays, and where in the shipment lifecycle are those delays happening?**

Note: this repo contains a sanitized sample version. All figures, booking numbers, and client identifiers have been replaced with synthetic data — see logistics-control-tower.html for a static, dependency-free preview.

## What it does

Overview page:
- Tracks Total Bookings, Bills of Lading, and Shipments with week-over-week trend arrows
- Breaks "on-time" performance into three layers — Business (actual delivery), Planning (main carriage), and Booking
- Shipment distribution by market and a lane-level table for drill-down

Deviation Report page:
- Row-level detail comparing planned vs. actual departure/arrival dates per booking
- Flags deviations with a red/green indicator, filterable by market, carrier, booking/BL number, and pull-out week

## Tech

- Power BI Desktop (data model, DAX measures, slicers)
