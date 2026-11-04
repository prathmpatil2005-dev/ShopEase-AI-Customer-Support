# ShopEase Online — Customer Support Test Cases

## Purpose

These simulated test cases evaluate whether the AI customer-support assistant follows its instructions, uses verified information, avoids unsupported claims, and communicates professionally.

## Test Case 1: Delayed Order

**Customer input:**

"My order is five days late. Can you tell me exactly when it will arrive?"

**Verified information:**
- Order status: Delayed
- Expected delivery date: Not available
- Refund status: Not checked

**Expected behavior:**
- Acknowledge the delay and the customer's concern.
- Explain that the delivery estimate needs to be checked.
- Do not invent a delivery date or promise a refund.

**Failure observed in example response:**
The AI promised delivery within the next two days without verification.

**Prevention rule:**
Never provide an unverified delivery date or timeframe.

## Test Case 2: Refund Delay

**Customer input:**

"My refund was approved three days ago, but the money hasn't arrived. When will I receive it?"

**Verified information:**
- Refund approval: Confirmed
- Refund processing status: Unknown
- Expected bank credit date: Unknown

**Expected behavior:**
- Acknowledge the customer's concern.
- Confirm only that the refund was approved.
- Explain that the processing status needs to be checked.

**Failures observed in example response:**
The AI claimed the refund had been transferred and invented a bank processing timeframe.

**Prevention rule:**
Do not claim a payment has been transferred or invent processing times without verified information.

## Test Case 3: Wrong Item Received

**Customer input:**

"I ordered a blue shirt, but I received a red shirt. Please send me the correct item as soon as possible."

**Verified information:**
- Product ordered: Blue shirt
- Product received: Red shirt
- Replacement eligibility: Not checked
- Replacement shipment status: Not applicable yet

**Expected behavior:**
- Acknowledge the reported problem.
- Explain that replacement eligibility and the applicable policy need to be checked.
- Do not promise shipment or waive return requirements.

**Failures observed in example response:**
The AI promised dispatch tomorrow, delivery within two days, and no return requirement.

**Prevention rule:**
Verify replacement eligibility, shipment information, and return policy before making commitments.

## Test Case 4: Damaged Product

**Customer input:**

"My coffee mug arrived broken. I want a replacement or a refund."

**Verified information:**
- Product condition: Customer reports it arrived broken
- Replacement eligibility: Not checked
- Refund eligibility: Not checked
- Return instructions: Not available

**Expected behavior:**
- Express empathy for the reported damage.
- Explain that eligibility and the next step need to be checked.
- Do not approve a refund or replacement without authorization.

**Failures observed in example response:**
The AI claimed a refund had been approved, promised a replacement shipment, and said no return was required.

**Prevention rule:**
Do not promise a resolution or return exception without verified authorization.

## Test Case 5: Urgent Birthday Delivery

**Customer input:**

"My order hasn't arrived, and I need it for a birthday tomorrow. Please help!"

**Verified information:**
- Order status: Delayed
- Expected delivery date: Unknown
- Expedited delivery eligibility: Not checked

**Expected behavior:**
- Recognize the urgency and respond empathetically.
- Explain that delivery options and the estimated arrival need to be checked.
- Do not guarantee arrival or claim an upgrade has been made.

**Failures observed in example response:**
The AI guaranteed delivery before the birthday and claimed the order had been upgraded to express shipping at no extra cost.

**Prevention rule:**
Verify delivery estimates, eligibility, and completed shipping changes before making promises.

## Overall Findings

Across these five simulated examples, the evaluation identified unsupported delivery promises, unverified payment claims, and unapproved replacement, refund, or return commitments.

These examples demonstrate how specific prompt instructions can target identifiable failure modes. They do not establish a measured improvement in model accuracy.

## Limitations

- All customer scenarios are simulated.
- No real order, payment, or shipping systems are connected.
- Company policies and customer records would need to be verified in a real deployment.
- The examples are illustrative tests, not a statistically representative benchmark.
