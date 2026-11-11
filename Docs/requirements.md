Part B

Functional Requirements:

Functional requirements define the core actions and capabilities the platform must provide to ensure proper parcel sizing and vehicle matching.

Requirement ID & Requirement Description

FR1:

The system shall require senders to input package dimensions (Length, Width, Height) or select a standard package preset during order creation.

FR2:

The system shall calculate the volumetric size and weight of each parcel using the entered dimensions.

FR3:

The system shall automatically block motorcycle dispatch and require a 4-wheel vehicle whenever package dimensions exceed motorcycle safety limits.

FR4:

The system shall display a spatial hazard badge on the rider app job preview screen before a rider accepts an order.

FR5:

The system shall allow riders to submit a photo-verified dimension mismatch report at pickup to unassign an unsafe job without penalty.


Non-Functional Requirements:

Non-functional requirements set the performance, usability, and operational standards the system must satisfy.

Requirement ID & Requirement Category & Measurable Condition
NFR1: Performance: 
The DSS spatial matching engine shall evaluate package dimensions and assign the vehicle type in under 1.5 seconds.
NFR2: Usability:
The rider hazard badge shall use high-contrast formatting that remains legible on standard mobile screens under daylight conditions.
NFR3: Reliability:
The spatial rule calculation engine shall maintain a 99.9% uptime during peak delivery operational hours.


User Stories and Acceptance Criteria:

User stories illustrate how different users interact with these features to achieve specific goals, supported by testable acceptance conditions.

Story ID: US1

User Story: As a merchant, I want to select preset item sizes (like Tall Bakery Box), so that I can place delivery orders quickly without measuring manually.

Linked Requirement: FR1

Acceptance Criteria:

1. Selecting a preset automatically fills in default maximum dimensions.
2. Leaving dimensions blank prevents the order from being submitted.

Story ID: US2

User Story: As a motorcycle rider, I want to see item size badges before accepting a job, so that I don't accept orders that won't fit in my storage box.

Linked Requirement: FR2

Acceptance Criteria:

1. The job offer screen shows the visual hazard badge and dimensions upfront.
2. Delicate or wide items highlight clear safety warnings in amber text.

Story ID: US3

User Story: As a motorcycle rider, I want to report oversized items at pickup, so that my cancellation rate isn't penalized for unsafe cargo.

Linked Requirement: FR3

Acceptance Criteria:

1. Tapping "Report Oversized Item" prompts a quick photo upload.
2. Submitting the report immediately unassigns the job with zero penalty and re-routes it to a car.
