# Test Cases

This file documents fictional test cases used to evaluate the AI customer operations assistant.

All examples are fictional and contain no real customer or company information.

---

## Test Case 1 — Delayed Railcar Pickup

### Customer Message

> Hi, we have railcars MXTX123456 and MXTX789012 ready for pickup at our facility. They've been waiting since yesterday and we need to know when they will be collected. Please let us know as soon as possible.

### Expected Behavior

The AI should:

* Identify this as a pickup request.
* Extract both railcar numbers.
* Classify the request as high priority because the railcars have been waiting since yesterday.
* Recommend checking the pickup status with Operations.
* Avoid promising a pickup time that has not been confirmed.

### Result

The AI classified the request as **High priority** and correctly identified the two railcars, the customer concern, and the required operational follow-up.

---

## Test Case 2 — Routine Shipment Status

### Customer Message

> Hello, could you please provide an update on shipment ORD-45218? There haven't been any issues; we would just like to know the current status. Thank you.

### Expected Behavior

The AI should:

* Identify this as a shipment status inquiry.
* Extract the shipment/order number.
* Classify the request as low priority because no problem or delay was reported.
* Recommend checking the shipment record and providing the customer with the confirmed status.

### Result

The AI classified the request as **Low priority** and correctly identified the request as a routine status inquiry.

---

## Test Case 3 — Delivery Delay Affecting Operations

### Customer Message

> Hello, our shipment was scheduled for delivery yesterday, but it still hasn't arrived. This shipment is needed for a production order and the delay is affecting our operations. Can you please investigate and let us know what is happening?

### Expected Behavior

The AI should:

* Identify this as a delivery delay or shipment investigation.
* Classify the request as high priority.
* Recognize that the delay is affecting the customer's operations.
* Recommend investigating the shipment status and cause of the delay.
* Identify that the shipment or order number is missing.
* Avoid inventing a shipment number or delivery status.

### Result

The AI classified the request as **High priority**, recognized the operational impact, and correctly identified that a shipment identifier was needed before the issue could be investigated.

---

## What I Learned From Testing

The initial version of the prompt classified the delayed railcar pickup as medium priority.

I identified that the priority instructions were too open to interpretation, so I added explicit criteria for Low, Medium, and High priority.

After updating the prompt, the same test case was classified as High priority.

Additional tests showed that the revised prompt could distinguish between routine status requests and operationally significant delays.

This experiment showed me that clear decision criteria are important when designing AI-assisted workflows and that testing with different scenarios is necessary before relying on an AI output.



## Test Case 4 — Rail Interchange Status

### Customer Message

> Hello, we want an update on two of our units, SFX999 and SFX888 we last knew that their location was where the exchange with the second rail company would take place 1 day ago, they tell us they have not received the units, we would like to know where they are and when would the exchange take place.

### My Expected Behavior

I expected the AI to:

* Identify this as a shipment status and railcar location inquiry.
* Recognize that the situation involves an interchange between rail companies.
* Treat the request as high priority because the expected interchange has already been missed.
* Recommend checking the latest movement and interchange records.
* Avoid assuming the current location of the units.
* Identify missing information that would be needed to investigate the issue.

### Result

The AI classified the request as **High priority** and identified the main issue correctly.

It recommended checking the latest tracking and interchange records and correctly identified that information such as the current location, exchange location, and relevant shipment details was missing.

I agreed with the AI's assessment because it matched the operational situation described in the customer message without making unsupported assumptions.

### What This Test Added

This scenario was created independently as an additional test of the workflow.

It helped me evaluate whether the prompt could handle a more specific logistics scenario involving an interchange between rail companies rather than a simple pickup or delivery request.
