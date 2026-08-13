# Learning Notes

## Why I Built This

I created this project to explore how AI could support customer operations workflows.

My previous experience in customer service and logistics involved handling customer requests, checking operational information, coordinating with internal teams, and following up on issues.

I wanted to experiment with how an AI assistant could help organize unstructured customer requests and identify the next operational action.

## What I Started With

I began with a simple prompt asking an AI model to analyze customer operations messages and identify the request type, priority, customer concern, required action, and recommended next step.

## First Test

In the first test, a customer reported that two railcars had been waiting for pickup since the previous day.

The AI classified the request as Medium priority.

I considered this too low because the customer had already experienced a delay and was requesting prompt action.

## What I Changed

I revised the prompt by adding explicit criteria for Low, Medium, and High priority.

I also instructed the AI to explain uncertainty rather than making unsupported assumptions.

## Second Test

After the change, the same customer request was classified as High priority.

The AI also explained that the railcars had been waiting longer than expected, which matched the criteria added to the prompt.

## Additional Testing

I tested the revised prompt with two additional scenarios:

1. A routine shipment status request with no reported problems.
2. A delayed delivery that was affecting a customer's production operations.

The AI classified the routine status request as Low priority and the operationally significant delivery delay as High priority.

It also correctly identified missing information instead of inventing details.

## What I Learned

This project helped me understand that working with AI is not only about writing a single prompt and accepting the first answer.

I learned that:

* Clear instructions lead to more consistent results.
* Decision criteria need to be explicitly defined when an AI system is making classifications.
* Testing the same workflow with different scenarios helps identify weaknesses.
* AI should identify missing information instead of filling gaps with assumptions.
* Human review remains important when AI outputs could influence operational decisions.

## What I Would Improve Next

If I continued developing this project, I would explore:

* Connecting the workflow to a form or automation platform.
* Adding more customer request categories.
* Testing the workflow with a larger set of scenarios.
* Measuring how consistently the AI classifies requests.
* Adding human approval before an AI-generated response is sent to a customer.

## Project Status

This is a small personal learning experiment.

The examples are fictional and do not contain real information.
