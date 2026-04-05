# Method

## What The Tool Is Trying To Predict

The tool is trying to identify which trusts are likely to experience the most severe pressure in the **next month**.

The main outcome used is:
- next-month `12+ hour waits from decision to admit`

You do not need to know the full NHS reporting detail to understand the idea.

In plain terms, this is being used as a marker of serious system pressure.

## What Data It Uses

The project uses public NHS data on:
- A&E attendances and emergency admissions
- bed occupancy
- discharge backlog

## What Goes Into The Score

The score combines 5 signals:
- current 12+ hour waits
- current 4-hour breach rate
- adult bed occupancy
- discharge backlog
- emergency admissions through A&E

These are then grouped into 3 simple operational categories:
- `Demand`
- `Flow`
- `Capacity`

## What Those Categories Mean

`Demand`
- pressure caused by high incoming emergency demand

`Flow`
- pressure caused by patients not moving through the hospital quickly enough

`Capacity`
- pressure caused by limited bed availability or high occupancy

## How The Weights Were Set

The weights were not chosen by hand.

Instead, each component was weighted by how strongly it related to next-month severe pressure in the historical validation period.

That makes the final score easier to defend because the weighting is based on observed signal, not preference.

## What The Tool Was Compared Against

The score was tested against two simple comparison methods:
- last month's 12-hour wait rate
- rolling 3-month average 12-hour wait rate

## Main Test

The main test was simple:

If you rank trusts from highest risk to lowest risk, does the model’s **top 10% risk group** contain more of next-month severe pressure than the simpler comparison methods?

That is why the result is expressed as “how much of next-month severe pressure sat inside the top 10% highest-risk trusts.”

## Time Period

The public data covered:
- `2025-01` to `2026-02`

That gave:
- 14 months of data
- 13 month-to-next-month validation windows

## Calibration Check

The trusts were also split into:
- `Low`
- `Medium`
- `High`

The question was:

Do the higher-risk bands actually show worse next-month outcomes?

In the final output, they do.

## Intended Use

This tool is for:
- trust-level prioritisation
- planning
- escalation discussion
- oversight

## What This Is Not

This is not:
- a patient-level prediction tool
- a causal model
- an automated decision system

## Main Limitation

The data is public and trust-level.

That makes it useful for system-level prioritisation, but not for patient-level operational decisions.
