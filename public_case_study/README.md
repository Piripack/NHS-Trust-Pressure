# NHS Trust Pressure: Public Case Study

This project asks one simple question:

**Which NHS trusts are most likely to face the worst severe pressure next month?**

It then asks two more:
- **What seems to be driving that pressure?**
- **Which simple operational change looks most helpful?**

This public case study is written for readers who may have no healthcare data background.

## What This Project Does

Using public NHS operational data, the project:
- ranks trusts by next-month pressure risk
- shows whether the main issue looks like `Demand`, `Flow`, or `Capacity`
- gives a clear action line
- compares 3 simple scenario tests

Those scenario tests are:
- `+5% discharges`
- `+5% available beds`
- `-5% admissions`

## What The Main Result Means In Plain English

When the model flagged the **top 10% of trusts as highest risk**, those trusts contained about **31% of all next-month severe pressure** on average.

The best simple baseline captured about **25%**.

So the model performed about **25% better than the best simple method you could use without the full model**.

It also beat the best simple method in **12 of the 13 months tested**.

## Why That Matters

This means the tool is not just describing the present.

It is useful for:
- spotting which trusts may need closer attention next month
- explaining whether the issue looks more like demand, flow, or capacity
- giving a practical way to structure planning and escalation discussions

## What To Read First

1. [dashboard.html](./dashboard.html)
2. [METHOD.md](./METHOD.md)
3. [RESULTS.md](./RESULTS.md)

## What Is Included Here

This public package includes:
- a simple visual dashboard
- a short method note
- a short results note
- selected sample outputs

## What Is Not Included

The full private implementation is not published in this folder.

This folder is meant to show:
- the problem
- the method at a high level
- the validation
- the outputs
- the practical use case

It is not meant to publish the full scoring engine.
