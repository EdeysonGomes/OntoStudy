The ontology encodes two inference rules, which are expressed as property chain axioms and annotated with the `DASE_RULE` annotation property.

*   **R1:** `hasBrother(?x, ?y) ^ hasMother(?x, ?m) -> hasMother(?y, ?m)`

    This rule states that if person *x* has a brother *y* and person *x* has a mother *m*, then person *y* also has mother *m*.
*   **R3:** `hasBrother(?x, ?y) ^ hasFather(?y, ?f) -> hasFather(?x, ?f)`

    This rule states that if person *x* has a brother *y* and person *y* has a father *f*, then person *x* also has father *f*.


The inference rules are mapped to Description Logic (DL) using **property chain axioms**.

*   In DL, a property chain axiom allows you to infer the existence of a relationship between two individuals based on the existence of a chain of relationships between them. For example, the property chain axiom `hasBrother o hasFather -> hasFather` states that if an individual *x* has a brother *y*, and *y* has a father *f*, then *x* also has father *f*.

*   The rules **R1** and **R3** are represented in the ontology using this mechanism. The `owl:propertyChainAxiom` construct is used to define the chain of properties, and the `DASE_RULE` annotation property is used to provide a human-readable representation of the rule.

Let's examine the DL mapping for **R1**:

*   **R1 in DASE:** `hasBrother(?x, ?y) ^ hasMother(?x, ?m) -> hasMother(?y, ?m)`
*   **R1 in DL:** The `owl:annotatedTarget` for `hasMother` includes `[ owl:inverseOf :hasBrother ]` followed by `:hasMother`. This signifies that if you traverse the inverse relationship of `hasBrother` from individual *y*, then follow the `hasMother` relationship, it implies that individual *y* also has the same `hasMother` relationship.

The DL mapping for **R3** follows a similar pattern:

*   **R3 in DASE:** `hasBrother(?x, ?y) ^ hasFather(?y, ?f) -> hasFather(?x, ?f)`
*   **R3 in DL:** The `owl:annotatedTarget` for `hasFather` includes `:hasBrother` followed by `:hasFather`. This indicates that starting from individual *x*, traversing the `hasBrother` relationship to *y*, and then following the `hasFather` relationship leads to the inference that individual *x* also shares the same `hasFather` relationship.

