# Results

## The Short Version

The model worked well enough to be useful as a trust-level early-warning tool.

In plain English:
- when the model flagged the **top 10% of trusts as highest risk**
- those trusts contained about **31% of all next-month severe pressure**

The best simple comparison method captured about **25%**.

So the model performed about **25% better than the best simple comparison method** on the main ranking test.

It also beat the best simple comparison method in **12 of the 13 months tested**.

## Why This Matters

That means the score is doing more than simply repeating recent history.

It is giving a more useful trust ranking than the simpler comparison methods used in the test.

## Calibration

The score was also checked using 3 bands:
- `Low`
- `Medium`
- `High`

Average next-month severe pressure rose clearly across those bands:

| Risk Band | Average Next-Month Severe Pressure |
|---|---:|
| Low | 92.7 |
| Medium | 299.7 |
| High | 777.9 |

That matters because it shows the bands match what happens later. Higher-risk bands really do have worse next-month outcomes.

## What The Trust Output Looks Like

For each trust, the output gives:
- a risk score
- a risk band
- a dominant driver
- an explicit action line
- a best scenario lever

Example:

`Driver: Flow. Action: Discharge acceleration / discharge coordination.`

## What The Scenario Layer Adds

The project does not only rank trusts.

It also asks:
- would risk fall more if discharges improved?
- would risk fall more if beds increased?
- would risk fall more if admissions fell?

That makes the output more useful for planning and discussion.

## Bottom Line

This project shows a trust-level tool that can:
- identify where next-month severe pressure may concentrate
- explain the likely reason
- suggest the most promising simple operational lever
