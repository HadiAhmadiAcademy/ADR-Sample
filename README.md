# ADR-001: Bubble Context For Integration With Legacy Accounting System

### Status

Accepted

### Context

We need to integrate our new system with an existing legacy **Accounting** system. The legacy system, built on outdated technology, operates with a horrible data model and uses a pretty meaningless domain language that could influence the new model and also introduce complexity and potential conflicts when integrated with our modernized system.

### Decision

We are going to create a "bubble" context for integrating the legacy **Accounting** system with our new system. This context reads **data directly from the legacy system's database**, incorporates a **translation layer** to handle model and language differences, and enforces a **one-way data flow** to protect our new system from legacy influences.

<figure><img src=".gitbook/assets/ADR-001-Bubble-Context" alt=""><figcaption></figcaption></figure>

### Consequences

As the bubble context introduces a middle layer, it'll add **maintenance effort** to keep it aligned with **both systems' changes**. However we believe that this overhead is justified by the benefits of isolation and protection from legacy influences.

### Compliance

* **Bubble Context Encapsulation (Manual):** verify proper implementation of the dedicated "bubble" context to encapsulate the integration in 3 aspects: **Mechanism**, **Model** & **Language**.
* **Unidirectional Data Flow (Manual):** Validating that the data flow within the bubble context is strictly unidirectional, preventing any direct impact on the legacy system.

### Notes

* Original Author: Olivia Rodriguez
* Approval Date: 2014-02-28
* Approved By: Ethan Thompson
* Last Modified Date:  2014-03-15
* Modified by: Olivia Rodriguez

