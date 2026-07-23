# Strength Management Tool — Case Study

## Overview
The Strength Management Tool is a Power BI readiness dashboard suite that
consolidates multiple personnel-system exports into a single analytical model.
It gives leaders a clear picture of authorized versus assigned strength,
projected gains and losses, and unit fill over time — the inputs that drive
readiness reporting.

## Problem
Strength management draws from several personnel-system exports, each with a
different structure and level of detail. There is no single view of
authorized-versus-assigned by unit, grade, and specialty, and no easy way to
project future strength as Soldiers arrive and depart. Rebuilding this picture
by hand every reporting cycle is slow, inconsistent, and error-prone.

## Solution
I designed an analytical model built on sound data-warehouse principles:
- A **snapshot model** that preserves every dated export, so the tool supports
  both point-in-time and trend analysis — a Power Query folder connector stamps
  each import with its report date automatically
- A **star schema** — separate fact tables for each report grain, with conformed
  dimensions for the unit-rollup hierarchy, date, rank/grade, and specialty
- **Force-projection modeling** that blends known and projected losses with
  inbound gains to produce a forward strength "glide path" as of any chosen date
- **Readiness views** by unit rollup, grade band (company grade, field grade,
  and enlisted skill levels), and specialty

## My Role
I served as the data architect and developer. I designed the star-schema
model, built the Power Query pipelines — including logic to handle irregular,
multi-block source exports and to correctly exclude internal moves from gain and
loss counts — authored the DAX measure library, and structured the dimensional
model around real force-management reporting needs.

## Impact
- A single source of truth for authorized, assigned, gains, and losses
- Point-in-time and trend analysis through the snapshot model
- Forward strength projection to support planning decisions
- Faster, more accurate, more consistent readiness inputs

## Why This Matters for ASWF
This project demonstrates my ability to:
- Design an enterprise-style data warehouse (star schema, snapshot modeling)
- Engineer resilient ETL pipelines from fragmented, imperfect source data
- Build DAX analytics that turn raw personnel data into decision-ready insight
- Deliver tooling that directly supports readiness and force management

*Built with Power BI (Power Query, DAX) using a snapshot star-schema
architecture. Developed and demonstrated with non-sensitive sample data.*

<!-- Screenshots: add dashboard images to the PowerBI-Dashboards section and
     link them here once captured from the sample-data build. -->
