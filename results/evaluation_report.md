# ShopEase Online — AI Response Evaluation Report

## 1. Report Overview

**Project:** ShopEase Online AI Customer Support Assistant  
**Evaluation type:** Manual, scenario-based prompt testing  
**Scenarios reviewed:** 5  
**Purpose:** Identify unsupported claims in sample AI-generated customer-support emails and define prompt rules to prevent them.

## 2. Test Results

| Test case | Main failure identified | Unsupported claims identified |
|---|---|---:|
| Delayed order | Unverified delivery timeframe | 1 |
| Refund delay | Unverified payment transfer and bank timeframe | 2 |
| Wrong item received | Unverified dispatch, delivery, and return-policy claims | 3 |
| Damaged product | Unverified refund approval, replacement shipment, and return exception | 3 |
| Urgent birthday delivery | Guaranteed arrival and unverified express-shipping upgrade | 2 |
| **Total** | | **11** |

These counts represent unsupported claims identified in the five example responses. They are not a model-wide error rate or a statistically validated performance measure.

## 3. Key Findings

### Finding 1: Unsupported delivery promises

The sample responses supplied delivery dates or timeframes without verified delivery information.

**Recommended prompt rule:** Do not provide a delivery date or timeframe unless it is supported by verified company records.

### Finding 2: Unverified financial claims

The refund-delay response claimed the payment had been transferred and supplied an unverified bank processing timeframe.

**Recommended prompt rule:** Distinguish refund approval from payment transfer and bank credit. State only the status supported by verified information.

### Finding 3: Unapproved resolutions

The wrong-item and damaged-product responses promised replacements, refunds, or return exceptions without confirming eligibility or authorization.

**Recommended prompt rule:** Do not promise a resolution until eligibility and approved company policy have been checked.

### Finding 4: Unsupported claims about completed actions

The birthday-delivery response claimed an express-shipping upgrade had already been made.

**Recommended prompt rule:** Never claim an action has been completed unless the available information confirms it.

## 4. Prompt Improvements

The reusable prompt was designed to emphasize:

- Verified facts only
- No invented dates or timelines
- No unapproved refunds, replacements, or exceptions
- Clear next steps when information is unavailable
- Human review when a resolution cannot be determined from verified information

These rules target the specific failure modes observed in the example responses. Their effectiveness must be confirmed through further testing.

## 5. Limitations

- All scenarios and responses were simulated.
- The five examples do not represent a statistically sampled dataset.
- The evaluation was manual.
- No live order-management, payment, or shipping system was connected.
- No before-and-after pass-rate comparison has been completed.
- Real deployment would require approved company policies, verified records, privacy safeguards, and appropriate human review.

## 6. Future Work

1. Generate and save the actual AI response for each test case using the reusable prompt.
2. Score every response against the evaluation checklist.
3. Record evidence and pass/fail results for each criterion.
4. Revise the prompt when failures occur and rerun the tests.
5. Compare original and revised prompts using the same test cases.
6. Expand the dataset and calculate a documented evaluation pass rate.

## 7. Conclusion

This project demonstrates a structured approach to prompt design, hallucination prevention, scenario-based testing, and manual evaluation of AI-generated customer-support emails.

The results document specific failure modes and corresponding prevention rules. Further controlled testing is needed to measure how reliably the improved prompt prevents these failures.
