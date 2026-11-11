Fundamental Concepts and System Operation: 

A Decision Support System (DSS) is an information framework that processes rules and data inputs to assist humans in making better decisions or to automate operational choices. In traditional gig delivery platforms, vehicle matching relies primarily on parcel weight and travel distance. This system introduces a spatial DSS that evaluates parcel volume against vehicle storage limits before dispatching a job.

[ Merchant Input: L x W x H ] ──► [ DSS Spatial Rule Engine ] ──► [ Automated Vehicle Match ] ──► [ Rider UX Display ]

The system operates across three core layers:
- Data Management Subsystem: Stores baseline storage dimensions for standard motorcycle delivery bags (40cm40cm40cm) and four-wheeled vehicle cargo space.
- Model & Rule Base (DSS Engine): Receives package dimensions (LWH) entered by the sender, computes volumetric size, and evaluates whether the item exceeds safe motorcycle handling thresholds.
- User Interface Subsystem (UX): Takes the decision output from the DSS engine and translates it into simple visual indicator, such as blocking motorcycle dispatch on the sender's screen or displaying spatial hazard badges ([COMPACT], [BULKY]) on the rider's job offer preview.

Frameworks, Models, Methods, and Tools: 

The implementation of this technology relies on three primary methods and frameworks:
- Volumetric Weight Calculation Model (IATA Standard): An industry-standard logistics formula used to compute dimensional weight (VolumetricWeight=(L x W x H) / 5000) . This model ensures lightweight but physically bulky items (like large hollow boxes or multi-tier cake boxes) are categorized accurately rather than treated as small items.
- Rule-Based Decision Engines: A heuristic logic engine (using simple conditional evaluation rules such as IF Volume > Bag Limit OR Width > 40cm THEN Reassign to Car) that processes order data in real time without heavy computational overhead.
- User-Centered Design (UCD) Framework & Figma: A UI/UX design methodology used to create intuitive mobile screens. It focuses on reducing cognitive load for riders on the road by presenting critical delivery information through high-contrast visual badges and minimal text.

Fit to Problem, Benefits, Limitations, and Alternative Comparison System Fit & Benefits:

Combining a DSS with improved UX directly solves the root cause of the delivery hazard. By shifting from a weight-only system to a spatial decision model, the platform automatically filters out dangerous items during order placement. Senders receive immediate guidance on appropriate vehicle selection, riders avoid physical hazards and unfair cancellation penalties, and merchants experience far fewer damaged goods during transit.


Limitations and Risks:
- Reliance on Accurate User Data Entry: The DSS depends on senders providing true package dimensions. If a merchant enters incorrect measurements to get a cheaper motorcycle delivery, inaccurate data will pass through the rule engine. (This risk is mitigated by allowing riders to submit photo-verified dimension mismatch reports at pickup).
- Sender Friction and Cost Resistance: Forcing oversized items to 4-wheel vehicles increases delivery fees for senders, which may cause temporary resistance or attempt to bypass mandatory fields.

Comparison with Alternative Approach (Computer Vision / Multimodal AI):

An alternative specialized technology for this problem is Computer Vision / Multimodal AI, where senders upload a photo of the parcel and an AI model estimates dimensions automatically.While Computer Vision reduces manual typing for senders, Option 6 (DSS + UX) is selected for this project. Rule-based DSS offers 100\% mathematical accuracy without requiring expensive machine learning infrastructure, complex model training, or background cloud processing. It provides immediate, predictable results using simple mobile interface fields, making it the most practical and reliable choice for a junior engineering project.
