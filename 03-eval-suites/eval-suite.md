# Eval Suite · wrong pricing

## P0 failure (carried from Module 2)

**Failure:** wrong pricing (#HALLUCINATION). Wrong Pricing for customers

- **Row:** 1
- **Query:** What is InsightFlow's pricing for Enterprise?
- **Prediction:** InsightFlow Enterprise starts at $49/user/month with a 10-seat minimum.
- **Reference:** Source: Pricing Page (Cached). Old Price: $49/mo. New Price (Updated yesterday): $59/mo.

## The three checks

**Rule check.** Looks at: answer. Passes when: Pricing for InsightFlow Enterprise starts at $49/user/month with a 10-seat minimum. Fails when: No Pricing for InsightFlow Enterprise starts at $49/user/month with a 10-seat minimum.

**Safety rule.** Looks at: answer. Passes when: It shouldn't mention competitor enterprise pricing Fails when: If its mention competitor enterprise pricing

**Judge.** Looks at: . Passes when: Pricing InsightFlow Enterprise Fails when: when it doesn't mention Pricing InsightFlow Enterprise

## Results on the 20 Ascend IQ answers

| Check | Caught | Missed (rows) | False alarms (rows) | My P0 row |
|---|---|---|---|---|
| Rule check |  |  |  |  |
| Safety rule |  |  |  |  |
| Judge |  |  |  |  |

## Where the failure was caught

Failure cot at Pricing, 1

## What I'd ship next

Pricing correctness is important for this to ship

## Row by row

| Row | Rule | Safety | Judge | Judge reason |
|---|---|---|---|---|
