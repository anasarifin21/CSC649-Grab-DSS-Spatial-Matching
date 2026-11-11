Part A

Problem Statement
In the gig economy, motorcycle delivery riders working for platforms like Grab, Lalamove, or Foodpanda are regularly assigned parcel deliveries that exceed safe physical handling limits. While current platform algorithms calculate delivery feasibility based almost entirely on package weight, they completely ignore spatial dimensions and volumetric bulk. As a result, riders are frequently assigned items such as multi-tier birthday cakes, wide catering trays, or large rigid boxes that cannot fit inside a standard motorcycle delivery bag.

This oversight creates a severe safety hazard. For example, a rider attempting to transport an 8-inch bakery cake is often forced to hold the box in one hand while operating the motorcycle with the other. Riding one-handed severely impairs balance, steering control, and emergency braking, directly endangering the rider’s life and increasing the risk of damaged goods. Furthermore, riders who reject these unsafe orders at pickup are penalized by automated cancellation rating systems. Without a mechanism to detect and block spatially unsuitable items during order placement, motorcycle riders remain exposed to avoidable road hazards.

Users and Stakeholders
To design an effective solution, the system identifies three main categories of users and stakeholders:

Motorcycle Delivery Riders (Primary Users): Frontline gig workers who receive job dispatches, inspect cargo upon pickup, and execute final delivery. Their main interest is personal safety, fair dispatching, and clear information before accepting jobs.
Merchants and Senders (Secondary Users): Bakeries, retail shops, and individual customers who place delivery orders. They require a straightforward ordering interface that accurately communicates their package needs without adding unnecessary complexity.
Platform Administrators (System Stakeholders): Operational teams who manage fleet dispatch rules, oversee driver support, and monitor overall platform safety metrics and cancellation policies.

Project Scope
To keep the project focused and feasible within a software development lifecycle, clear operational boundaries have been defined:

In-Scope: 
Senders entering mandatory parcel dimensions (LWH) or choosing preset package categories (e.g., Tall Bakery Box) during order creation.
A rule-based Decision Support System (DSS) spatial algorithm that calculates volumetric weight and compares it against standard motorcycle storage limits.
Automated vehicle re-routing to 4-wheel vehicles (cars/vans) when package dimensions exceed safe motorcycle limits.
Enhanced UI visual badges on the rider app to display spatial hazard alerts before job acceptance.
A 1-tap "Dimension Mismatch" photo reporting feature in the rider app to unassign unsafe jobs without rating penalties.

Out-of-Scope:
Real-time GPS navigation, dynamic route optimization, or traffic mapping.
Direct integration with external payment gateways or banking APIs.
Automated physical sensors or hardware-based volume scanners attached to motorcycles.
Chat backend systems between customers and riders.

