# ShopEase Online — AI Response Evaluation Checklist

## Purpose

This checklist provides a consistent way to evaluate AI-generated customer-support emails against the project's requirements.

## Evaluation Criteria

For each criterion, record Pass, Fail, or Not Applicable.

| ID | Criterion | Pass condition |
|---|---|---|
| E1 | Customer concern | The response addresses the customer's actual issue. |
| E2 | Factual accuracy | Claims are supported by provided facts or verified company records. |
| E3 | No invented timelines | No unverified delivery dates, payment timeframes, or shipping estimates are provided. |
| E4 | Authorized resolutions | Refunds, replacements, returns, and exceptions are not promised without verification and authorization. |
| E5 | Appropriate next step | The response explains a reasonable next step using available information and approved policy. |
| E6 | Empathy and professionalism | The response is respectful, clear, and appropriately empathetic. |
| E7 | Output format | The response follows the requested email format and any specified length requirements. |

## Evaluation Procedure

1. Read the customer's original email.
2. Review the verified information and identify what remains unknown.
3. Read the AI-generated response.
4. Evaluate each criterion independently.
5. Record unsupported claims and missing requirements.
6. Recommend a specific prompt improvement when a failure is found.
7. Retest the revised prompt using the same scenario and additional scenarios.

## Recording Results

Use this template for each test:

- **Test case ID:**
- **Criterion ID:**
- **Result:** Pass / Fail / Not Applicable
- **Evidence:** Quote or describe the relevant part of the AI response.
- **Reason:** Explain why the response passes or fails.
- **Recommended improvement:** Identify the instruction that should be clarified.

## Scoring Method

For a simple pass rate, count applicable criteria marked Pass and divide by the total number of applicable criteria evaluated.

Pass rate = Passed applicable criteria / Total applicable criteria × 100

A response with a critical unsupported promise should also be flagged separately, even if it passes several other criteria.

## Important Limitations

This checklist is a proposed evaluation framework. It has not yet been applied to a complete, independently recorded dataset of generated responses.

The example failures identified in this project are illustrative. More systematic testing is required before making claims about overall accuracy or improvements in AI performance.
