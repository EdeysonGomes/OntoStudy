# Genealogy Ontology Project

Welcome to the Genealogy Ontology Project! This repository serves as a resource to aid in the study of ontologies, with a focus on exploring and applying fundamental concepts using Protégé 5. The example ontology is based on the British royal family.

---

## **Project Objectives**

The primary objectives of this project are:

### 1. **Learning Ontological Concepts**
   - Introduce and deepen understanding of core ontology concepts such as:
     - Classes and Subclasses
     - Object Properties
     - Data Properties
     - Individuals (Instances)
     - Property Chains
     - Inference Rules
   - Understand the difference between TBox (terminological box) and ABox (assertional box).

### 2. **Exploring Genealogy Ontology**
   - Use a real-world example to demonstrate genealogical relationships:
     - Parental relationships (`hasFather`, `hasMother`, `hasParent`)
     - Sibling relationships (`hasBrother`, `hasSister`, `hasSibling`)
     - Gender classification (`hasGender`, `Male`, `Female`)
   - Illustrate family structures and hierarchies, emphasizing reasoning capabilities.

### 3. **Practical Ontology Development**
   - Employ Protégé 5 as a tool for:
     - Creating and managing ontologies.
     - Defining classes, properties, and axioms.
     - Executing reasoning tasks.
   - Showcase ontology reasoning with property chain axioms to infer relationships automatically.

### 4. **Case Study: British Royal Family**
   - Provide a comprehensive example based on the British royal family.
   - Include key family members such as Queen Elizabeth II, Prince Philip, Prince Charles, and others.
   - Demonstrate:
     - Explicit assertions (e.g., "Archie hasFather Harry").
     - Inferred relationships using logical rules (e.g., "If Archie hasFather Harry, and Archie hasBrother Lilibet, then Lilibet also hasFather Harry").

---

## **Repository Contents**

- **`Genealogia_x.ttl`**: The ontology file to be explored using Protégé (x is de version of the ontology).
- **`images/`**: Diagrams and visualizations of the ontology structure.
- **`examples/`**: Example queries and reasoning results.
- **`README.md`**: This file, providing project details and usage instructions.

---

## **Getting Started**

### 1. Prerequisites
   - Install [Protégé 5](https://protegeproject.github.io/) on your computer.
   - Familiarity with basic ontology terms and concepts is recommended.

### 2. Load the Ontology
   - Open Protégé 5.
   - Import the `Genealogia_x.owl` file from this repository (x is the version number of the ontology).

### 3. Explore and Reason
   - Examine the class hierarchy and properties.
   - Use the reasoner in Protégé to infer new relationships based on axioms and rules.
   - Review explicit assertions and inferred relationships in the individuals tab.

---

## **Examples of Use**

### **Exploring Family Relationships**
1. **Direct Assertions:**
   - Example: `hasFather(Archie, Harry)`
   - Example: `hasMother(Lilibet, Meghan)`

2. **Inferred Relationships:**
   - Using property chains:
     - If Lilibet hasBrother Archie, and Archie hasFather Harry, then Lilibet also hasFather Harry.
     - If Lilibet hasMother Meghan, then Lilibet hasParent Meghan.

### **Defining Gender**
- Every individual is linked to a `Gender` class (`Male` or `Female`) using the `hasGender` property.

---

## **Contributing**

Contributions to expand and refine this ontology are welcome! If you have suggestions, fixes, or additional features, please feel free to open an issue or submit a pull request.

---

## **License**

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## **Acknowledgments**

Special thanks to the Protégé team and the broader ontology research community for providing tools and resources that make projects like this possible.

---

Happy learning and exploring ontology development!

