# Software Engineering Exam Answers

## Question 1: Agility and Cost of Change

### a) Agility and Cost of Change Graph

**Software Agility** refers to the ability of a software development team or process to rapidly and effectively respond to changes. These changes can include evolving customer requirements, market opportunities, technological advancements, or feedback from stakeholders. Agile methodologies are designed to embrace change as a natural part of the development lifecycle, rather than resisting it. Key characteristics of agility include iterative development, incremental delivery, collaboration, flexibility, and continuous improvement.

**The Cost of Change Graph** illustrates how the cost of making changes to software evolves over the different phases of the development lifecycle.

*   **Traditional (Waterfall) Model:** In traditional models, the cost of change increases exponentially as the project progresses. Changes identified late in the lifecycle (e.g., during testing or after deployment) are significantly more expensive to implement. This is because early phases (requirements, design) are typically "frozen," and late changes can necessitate extensive rework of documentation, code, and testing efforts.
*   **Agile Model:** Agile methodologies aim to flatten this cost of change curve. By embracing iterative development, continuous feedback, and frequent deliveries, changes can be incorporated more easily and at a lower cost throughout the project. While the cost still rises, the increase is much more gradual compared to traditional models. Early and frequent feedback helps identify and address necessary changes when they are less impactful.

mermaid
graph TD
    subgraph Traditional Model
        direction LR
        X1[Time/Phases] --> Y1{Cost of Change};
        P1[Requirements] --> P2[Design] --> P3[Implementation] --> P4[Testing] --> P5[Deployment];
        C1[Low Cost] --> C2[Medium Cost] --> C3[High Cost] --> C4[Very High Cost] --> C5[Extremely High Cost];
        style Y1 fill:#f9f,stroke:#333,stroke-width:2px
        style P1 fill:#eee,stroke:#333
        style P2 fill:#eee,stroke:#333
        style P3 fill:#eee,stroke:#333
        style P4 fill:#eee,stroke:#333
        style P5 fill:#eee,stroke:#333
        linkStyle 0 stroke-width:2px,fill:none,stroke:red;
        subgraph Cost Curve Traditional
            direction LR
            CT1(Start) --> CT2(Low) --> CT3(Medium) --> CT4(Exponentially High) --> CT5(Very High)
            style CT1 fill:none,stroke:none
            style CT2 fill:none,stroke:none
            style CT3 fill:none,stroke:none
            style CT4 fill:none,stroke:none
            style CT5 fill:none,stroke:none
            %% This is a conceptual representation. Actual plotting requires x/y coordinates.
            %% For demonstration, imagine a steep upward curve.
        end
    end
   subgraph Agile Model
        direction LR
        X2[Time/Iterations] --> Y2{Cost of Change};
        I1[Iter 1] --> I2[Iter 2] --> I3[Iter N] --> ID[Deployment];
        CA1[Low Cost] --> CA2[Slightly Higher] --> CA3[Moderately Higher] --> CA4[Higher but Manageable];
        style Y2 fill:#ccf,stroke:#333,stroke-width:2px
        style I1 fill:#eee,stroke:#333
        style I2 fill:#eee,stroke:#333
        style I3 fill:#eee,stroke:#333
        style ID fill:#eee,stroke:#333
        linkStyle 5 stroke-width:2px,fill:none,stroke:blue;
         subgraph Cost Curve Agile
            direction LR
            CGA1(Start) --> CGA2(Low) --> CGA3(Gradual Increase) --> CGA4(Moderate) --> CGA5(Manageable)
            style CGA1 fill:none,stroke:none
            style CGA2 fill:none,stroke:none
            style CGA3 fill:none,stroke:none
            style CGA4 fill:none,stroke:none
            style CGA5 fill:none,stroke:none
            %% For demonstration, imagine a flatter, gradually rising curve.
        end
    end
    note right of Y1 : Cost rises sharply in later stages
    note right of Y2 : Cost rises more gradually

*(Conceptual diagram: The Mermaid graph above provides a structural representation. A true plot would show the y-axis (Cost) increasing much more steeply for Traditional vs. Agile over the x-axis (Time/Phases).)*

### b) Five P's of Agility

While various interpretations exist, a common set of "Five P's" contributing to agility includes:

1.  **People:** Emphasizes the importance of skilled individuals, collaboration, communication, trust, and empowerment within the team. Agile success heavily relies on motivated and self-organizing teams.
2.  **Process:** Refers to the agile methodologies and practices adopted (e.g., Scrum, Kanban, XP). These processes are typically lightweight, iterative, and flexible, allowing for adaptation.
3.  **Product:** Focuses on delivering value to the customer through working software. Agile prioritizes frequent delivery of functional product increments, allowing for early feedback and validation.
4.  **Project:** Pertains to how agile principles are applied to project management. This includes adaptive planning, continuous risk assessment, and stakeholder engagement throughout the project lifecycle.
5.  **Pace (or Performance/Preparedness):** Highlights the need for a sustainable pace of development that the team can maintain indefinitely. It also relates to the team's preparedness to handle changes and the overall performance in delivering value.

### c) Major Disadvantage of Agile Methodology over Traditional Approach

One of the major disadvantages of agile methodology, especially when compared to the traditional (Waterfall) approach, is the **potential for less predictability in terms of final scope, timeline, and budget at the very beginning of the project.**

*   **Traditional Approach:** Waterfall models emphasize detailed upfront planning. This often results in a clearer (though not always accurate) initial picture of the total scope, cost, and schedule. This can be preferable for clients or stakeholders who require a high degree of predictability and fixed contracts.
*   **Agile Approach:** Agile embraces change and iterative development. While this offers flexibility, it means that the full scope might not be defined at the outset. Requirements evolve, and priorities can shift based on feedback. This can make it challenging to provide precise long-term estimates for the entire project upfront. This can be a concern for projects with strict budgetary or timeline constraints, or where a fixed scope is non-negotiable from the start.

Other potential challenges include the need for high customer involvement, which may not always be feasible, and the requirement for experienced and disciplined teams.

---

## Question 2: Requirements Elicitation

### a) Requirements Elicitation Process

**Requirements Elicitation** is the process of discovering, gathering, and defining the requirements for a software system from various stakeholders, including users, customers, domain experts, and other relevant parties. It is a critical early phase in software development, as the quality and completeness of elicited requirements significantly impact the success of the project.

The process typically involves:

1.  **Identifying Stakeholders:** Determining who has an interest in or will be affected by the system.
2.  **Understanding the Domain:** Gaining knowledge about the business area or problem the software aims to address.
3.  **Gathering Information:** Using various techniques to collect raw requirements from stakeholders.
4.  **Analyzing and Negotiating:** Refining, clarifying, and resolving conflicts in the gathered information to produce a consistent set of requirements.
5.  **Documenting Requirements:** Recording the agreed-upon requirements in a clear, concise, and unambiguous manner (e.g., in a Software Requirements Specification - SRS).
6.  **Validating Requirements:** Ensuring that the documented requirements accurately reflect the stakeholders' needs and are feasible to implement.

### b) Four Standard Requirements Elicitation Techniques

1.  **Interviews:** Conducting one-on-one or small group discussions with stakeholders to gather their needs, expectations, and constraints. Interviews can be structured (predefined questions) or unstructured (more open-ended).
2.  **Workshops (e.g., JAD - Joint Application Development sessions):** Bringing together a diverse group of stakeholders (users, developers, managers) in a facilitated session to collaboratively define, refine, and agree upon requirements.
3.  **Prototyping:** Creating an early, partial version or model of the system (e.g., UI mockups, storyboards, or a working prototype with limited functionality). Stakeholders can interact with the prototype to provide feedback and clarify their needs, helping to uncover unstated or misunderstood requirements.
4.  **Document Analysis (or Review of Existing Systems/Documentation):** Examining existing documents, such as business process descriptions, organizational charts, policy manuals, user manuals of current systems, or competitor systems, to extract relevant requirements and understand the current environment.

### c) Advantages and Disadvantages of Requirements Elicitation

**Advantages:**

1.  **Clearer Understanding of Needs:** Helps to ensure that the development team has a comprehensive and accurate understanding of what the stakeholders truly need, reducing the risk of building the wrong system.
2.  **Improved Stakeholder Buy-in and Satisfaction:** Involving stakeholders in the process fosters a sense of ownership and increases the likelihood that the final product will meet their expectations, leading to higher satisfaction.

**Disadvantages:**

1.  **Time-Consuming and Potentially Costly:** The process of identifying all stakeholders, conducting interviews or workshops, and analyzing information can be lengthy and resource-intensive, especially for complex systems.
2.  **Difficulty in Articulating Needs (Stakeholder Problems):** Stakeholders may sometimes have difficulty expressing their needs clearly, may provide conflicting information, or may not fully understand the possibilities and limitations of technology, leading to incomplete or ambiguous requirements.

---

## Question 3: SFC (SRM Fee Calculator) - DFDs and Data Dictionary

### a) Data Flow Diagrams (DFD)

**Level 0 DFD (Context Diagram) for SFC Software**

mermaid
graph LR
    User([User]) -->|User Inputs: SRMJEE_Rank, Branch_Choice, Age, Accommodation_Type, Meal_Option, Gender| SFC_System((SRM Fee Calculator SFC));
    SFC_System -->|Total_Annual_Fee| User;
    style User fill:#dae,stroke:#333,stroke-width:2px
    style SFC_System fill:#ade,stroke:#333,stroke-width:4px


**Level 1 DFD for SFC Software**

mermaid
graph TD
    subgraph SFC System (Level 1)
        User_Input([User Inputs]) --> P1{1.0 Validate Inputs};
        P1 -- Validated Inputs --> P2{2.0 Calculate Base Tuition Fee};
        P2 -- Base Tuition Fee --> P3{3.0 Calculate Rank Discount};
        P1 -- Validated SRMJEE Rank --> P3;
        P3 -- Discounted Tuition Fee --> P4{4.0 Calculate Gender Discount};
        P1 -- Validated Gender --> P4;
        P4 -- Final Tuition Fee --> P6{6.0 Calculate Total Annual Fee};
        P1 -- Validated Accommodation Type --> P5{5.0 Calculate Ancillary Fees};
        P1 -- Validated Meal Option --> P5;
        P5 -- Total Ancillary Fees --> P6;
        P6 -- Total Annual Fee --> Output_Fee([Total Annual Fee Display]);
        DS_Branch_Fees[Branch Fees Data] --> P2;
        DS_Accommodation_Fees[Accommodation Fees Data] --> P5;
        DS_Meal_Fees[Meal Fees Data] --> P5;
        DS_Rank_Discounts[Rank Discount Rules] --> P3;
        DS_Gender_Discounts[Gender Discount Rules] --> P4;
        style User_Input fill:#dae,stroke:#333,stroke-width:2px
        style Output_Fee fill:#dae,stroke:#333,stroke-width:2px
        style P1 fill:#ade,stroke:#333,stroke-width:2px
        style P2 fill:#ade,stroke:#333,stroke-width:2px
        style P3 fill:#ade,stroke:#333,stroke-width:2px
        style P4 fill:#ade,stroke:#333,stroke-width:2px
        style P5 fill:#ade,stroke:#333,stroke-width:2px
        style P6 fill:#ade,stroke:#333,stroke-width:2px
        style DS_Branch_Fees fill:#fab,stroke:#333,stroke-width:2px
        style DS_Accommodation_Fees fill:#fab,stroke:#333,stroke-width:2px
        style DS_Meal_Fees fill:#fab,stroke:#333,stroke-width:2px
        style DS_Rank_Discounts fill:#fab,stroke:#333,stroke-width:2px
        style DS_Gender_Discounts fill:#fab,stroke:#333,stroke-width:2px
    end


**Level 2 DFD for Process 3.0 (Calculate Rank Discount)**

mermaid
graph TD
    subgraph Process 3.0 Calculate Rank Discount (Level 2)
        Input_BaseTuitionFee(Base Tuition Fee) --> P3_1{3.1 Determine Rank Category};
        Input_SRMJEE_Rank(Validated SRMJEE Rank) --> P3_1;
        DS_Rank_Discount_Rules[Rank Discount Rules] --> P3_1;
        P3_1 -- Rank Category, Discount Percentage --> P3_2{3.2 Apply Discount};
        Input_BaseTuitionFee --> P3_2;
        P3_2 -- Discounted Tuition Fee --> Output_DiscountedTuitionFee(Discounted Tuition Fee);
        style Input_BaseTuitionFee fill:#eee,stroke:#333
        style Input_SRMJEE_Rank fill:#eee,stroke:#333
        style Output_DiscountedTuitionFee fill:#eee,stroke:#333
        style P3_1 fill:#ade,stroke:#333,stroke-width:2px
        style P3_2 fill:#ade,stroke:#333,stroke-width:2px
        style DS_Rank_Discount_Rules fill:#fab,stroke:#333,stroke-width:2px
    end


### b) Data Dictionary for SFC Software

**Data Flows:**

1.  **User_Inputs:**
    *   Description: Composite data flow containing all inputs provided by the user.
    *   Composition: SRMJEE_Rank + Branch_Choice + Age + Accommodation_Type + Meal_Option + Gender
2.  **SRMJEE_Rank:**
    *   Description: Rank obtained by the student in SRMJEE.
    *   Type: Integer
    *   Range: 1 to 25000
3.  **Branch_Choice:**
    *   Description: Chosen engineering branch.
    *   Type: String
    *   Values: "CSE", "ECE", "MECH", "EEE", "Civil"
4.  **Age:**
    *   Description: Age of the student.
    *   Type: Integer
    *   Range: 18 to 23
5.  **Accommodation_Type:**
    *   Description: Type of accommodation chosen.
    *   Type: String
    *   Values: "AC", "Non-AC"
6.  **Meal_Option:**
    *   Description: Meal preference.
    *   Type: String
    *   Values: "Veg", "Non-Veg"
7.  **Gender:**
    *   Description: Gender of the student.
    *   Type: String
    *   Values: "Male", "Female", "Other"
8.  **Validated_Inputs:**
    *   Description: User inputs after validation checks.
    *   Composition: Same as User_Inputs, but confirmed to be within valid ranges/values.
9.  **Base_Tuition_Fee:**
    *   Description: Annual tuition fee before any discounts, based on branch.
    *   Type: Currency (Float/Decimal)
10. **Discounted_Tuition_Fee:**
    *   Description: Tuition fee after applying rank-based discount.
    *   Type: Currency (Float/Decimal)
11. **Final_Tuition_Fee:**
    *   Description: Tuition fee after applying all applicable discounts (rank and gender).
    *   Type: Currency (Float/Decimal)
12. **Total_Ancillary_Fees:**
    *   Description: Sum of accommodation and meal charges.
    *   Type: Currency (Float/Decimal)
13. **Total_Annual_Fee:**
    *   Description: The final computed total annual fee to be paid by the student.
    *   Type: Currency (Float/Decimal)
    *   Composition: Final_Tuition_Fee + Total_Ancillary_Fees
14. **Rank_Category:**
    *   Description: Category determined by SRMJEE rank for discount purposes.
    *   Type: String (e.g., "1-1000", "1001-10000")
15. **Discount_Percentage:**
    *   Description: Percentage of discount applicable based on rank or gender.
    *   Type: Float (e.g., 0.50 for 50%)

**Data Stores:**

1.  **DS_Branch_Fees:**
    *   Description: Stores the base annual tuition fee for each branch.
    *   Content: {Branch_Name, Tuition_Fee_Amount}
    *   Example: {"CSE", 300000}, {"ECE", 250000}, ...
2.  **DS_Accommodation_Fees:**
    *   Description: Stores annual charges for different accommodation types.
    *   Content: {Accommodation_Type_Name, Accommodation_Charge}
    *   Example: {"AC", 100000}, {"Non-AC", 75000}
3.  **DS_Meal_Fees:**
    *   Description: Stores annual charges for different meal options.
    *   Content: {Meal_Option_Name, Meal_Charge}
    *   Example: {"Veg", 60000}, {"Non-Veg", 70000}
4.  **DS_Rank_Discounts:**
    *   Description: Stores rules for tuition fee discounts based on SRMJEE rank.
    *   Content: {Rank_Range_Start, Rank_Range_End, Discount_Rate}
    *   Example: {1, 1000, 0.50}, {1001, 10000, 0.25}, ...
5.  **DS_Gender_Discounts:**
    *   Description: Stores rules for additional tuition fee discounts based on gender.
    *   Content: {Gender_Category, Discount_Rate}
    *   Example: {"Female", 0.05}, {"Other", 0.08}

**Processes (Brief Description):**

*   **1.0 Validate Inputs:** Checks if all user-provided inputs are within their specified valid ranges and formats.
*   **2.0 Calculate Base Tuition Fee:** Determines the initial tuition fee based on the selected branch using DS_Branch_Fees.
*   **3.0 Calculate Rank Discount:** Calculates the discount on tuition fee based on SRMJEE rank using DS_Rank_Discounts.
    *   **3.1 Determine Rank Category:** Identifies which discount tier the student's rank falls into.
    *   **3.2 Apply Discount:** Calculates the actual discount amount and the discounted tuition fee.
*   **4.0 Calculate Gender Discount:** Calculates any additional discount on the (potentially already rank-discounted) tuition fee based on gender using DS_Gender_Discounts.
*   **5.0 Calculate Ancillary Fees:** Calculates the sum of accommodation charges (from DS_Accommodation_Fees) and meal charges (from DS_Meal_Fees).
*   **6.0 Calculate Total Annual Fee:** Sums the final discounted tuition fee and the total ancillary fees to get the overall annual fee.

---

## Question 4: Cohesion and Coupling

### a) Cohesion and Coupling

**Cohesion:**
Cohesion refers to the degree to which the elements *within* a single module (e.g., a class, a function, a component) are related and work together to perform a single, well-defined task.
*   **High Cohesion:** Indicates that the module is focused on a specific responsibility, and all its internal parts contribute to that responsibility. This is desirable as it makes the module easier to understand, maintain, and reuse.
*   **Low Cohesion:** Indicates that the module performs many unrelated tasks or that its elements are loosely connected. This makes the module harder to understand, modify (as a change in one unrelated part might affect another), and reuse.

**Coupling:**
Coupling refers to the degree of interdependence *between* different modules. It measures how strongly one module is connected to, has knowledge of, or relies on another module.
*   **Low Coupling (Loose Coupling):** Indicates that modules are relatively independent. Changes in one module are less likely to affect others. This is desirable as it improves modularity, makes the system easier to maintain (changes are localized), and promotes reusability of individual modules.
*   **High Coupling (Tight Coupling):** Indicates that modules are heavily reliant on each other. A change in one module often necessitates changes in other dependent modules. This makes the system more rigid, harder to maintain, and less reusable.

### b) Illustrate the Concept of Modularity with Examples

**Modularity** is a software design principle that emphasizes breaking down a complex software system into smaller, independent, and interchangeable parts called modules. Each module encapsulates a specific part of the system's functionality and has a well-defined interface for interacting with other modules.

**Example 1: A Car**
A car is a highly modular system:
*   **Modules:** Engine, Transmission, Braking System, Electrical System, Entertainment System.
*   **Independence:** The engine can be designed, manufactured, and even replaced independently of the entertainment system (to a large extent).
*   **Well-defined Interfaces:** The engine connects to the transmission through a specific interface (e.g., driveshaft, clutch). The braking system interacts with the wheels through defined mechanisms.
*   **Benefits:**
    *   **Maintainability:** If the radio breaks, you can replace or repair the entertainment system module without affecting the engine.
    *   **Reusability/Replaceability:** A car manufacturer might use the same engine module in different car models.
    *   **Parallel Development:** Different teams can work on the engine and the interior design simultaneously.

**Example 2: A Web Application (e.g., E-commerce Site)**
*   **Modules:**
    *   **User Authentication Module:** Handles user login, registration, password recovery.
    *   **Product Catalog Module:** Manages product listings, search, and details.
    *   **Shopping Cart Module:** Allows users to add/remove items and view their cart.
    *   **Order Processing Module:** Handles checkout, payment, and order fulfillment.
    *   **Notification Module:** Sends emails or SMS for order confirmations, shipping updates.
*   **Independence:** The Product Catalog module can be updated with new products without directly changing the core logic of the User Authentication module.
*   **Well-defined Interfaces:** The Shopping Cart module might call an interface provided by the Order Processing module to initiate checkout. The Order Processing module might use an interface from the Notification module to send an email.
*   **Benefits:**
    *   **Understandability:** It's easier to understand the logic for user login if it's contained within a dedicated authentication module.
    *   **Testability:** Each module can be tested independently.
    *   **Scalability:** If product search becomes a bottleneck, the Product Catalog module can be optimized or scaled independently.

### c) Why "Low Coupling - High Cohesion is better for good software"

"Low coupling - High cohesion" is a fundamental principle for designing good quality software because it leads to systems that are:

1.  **More Maintainable:**
    *   **High Cohesion:** When a module has high cohesion, its internal logic is focused and related. If a change is needed for a specific functionality, it's likely to be localized within that cohesive module. This reduces the ripple effect of changes.
    *   **Low Coupling:** When modules are loosely coupled, a change in one module is less likely to necessitate changes in other modules. This isolation simplifies debugging and modifications, as developers can confidently change one part of the system without unintentionally breaking others.

2.  **Easier to Understand:**
    *   **High Cohesion:** A cohesive module has a clear, single purpose. It's easier for developers to grasp what the module does and how it works internally.
    *   **Low Coupling:** With low coupling, developers can understand a module by primarily focusing on its defined interface and its own internal logic, without needing to delve deeply into the implementation details of many other modules it might interact with.

3.  **More Reusable:**
    *   **High Cohesion:** Modules that perform a single, well-defined task are more likely to be useful in other parts of the system or even in different projects. Their specific focus makes them good candidates for reuse.
    *   **Low Coupling:** Modules with few dependencies on others can be easily taken and plugged into new contexts without dragging along a web of other interconnected modules.

4.  **More Testable:**
    *   **High Cohesion:** It's easier to write unit tests for a module that has a clear and focused responsibility.
    *   **Low Coupling:** Modules can be tested in isolation (or with minimal, well-defined stubs/mocks for their dependencies) if they are not tightly bound to many other parts of the system.

5.  **Increased Robustness and Reduced Ripple Effect:**
    *   **Low Coupling:** Faults or errors in one module are less likely to propagate to other modules if the connections between them are minimized and well-managed. This containment of errors improves the overall stability of the system.

In essence, striving for high cohesion within modules and low coupling between modules helps manage complexity, promotes flexibility, and results in software that is more adaptable to change over its lifecycle.

---

## Question 5: Electricity Bill Calculation

### a) Pseudocode

pseudocode
PROCEDURE CalculateElectricityBill
  INPUT: unitsConsumed (Integer)
  OUTPUT: electricityBill (Real)

  CONSTANT RATE_TIER1 = 3.00  // For 1 to 50 units
  CONSTANT RATE_TIER2 = 3.50  // For 51 to 100 units
  CONSTANT RATE_TIER3 = 4.75  // For 101 to 150 units
  CONSTANT RATE_TIER4 = 6.50  // For 151 units and above

  CONSTANT LIMIT_TIER1 = 50
  CONSTANT LIMIT_TIER2 = 100
  CONSTANT LIMIT_TIER3 = 150

  DECLARE billTier1, billTier2, billTier3, billTier4 AS Real
  SET billTier1 = 0
  SET billTier2 = 0
  SET billTier3 = 0
  SET billTier4 = 0

  IF unitsConsumed <= 0 THEN
    SET electricityBill = 0
  ELSE
    IF unitsConsumed > 0 THEN
      IF unitsConsumed <= LIMIT_TIER1 THEN
        billTier1 = unitsConsumed * RATE_TIER1
      ELSE // unitsConsumed > LIMIT_TIER1
        billTier1 = LIMIT_TIER1 * RATE_TIER1
        IF unitsConsumed <= LIMIT_TIER2 THEN
          billTier2 = (unitsConsumed - LIMIT_TIER1) * RATE_TIER2
        ELSE // unitsConsumed > LIMIT_TIER2
          billTier2 = (LIMIT_TIER2 - LIMIT_TIER1) * RATE_TIER2
          IF unitsConsumed <= LIMIT_TIER3 THEN
            billTier3 = (unitsConsumed - LIMIT_TIER2) * RATE_TIER3
          ELSE // unitsConsumed > LIMIT_TIER3
            billTier3 = (LIMIT_TIER3 - LIMIT_TIER2) * RATE_TIER3
            billTier4 = (unitsConsumed - LIMIT_TIER3) * RATE_TIER4
          END IF
        END IF
      END IF
    END IF
    SET electricityBill = billTier1 + billTier2 + billTier3 + billTier4
  END IF

  DISPLAY "Total Electricity Bill: ", electricityBill
END PROCEDURE


### b) Control Flow Graph (CFG)

mermaid
graph TD
    A[Start: Input unitsConsumed] --> B{unitsConsumed <= 0?};
    B -- Yes --> C[electricityBill = 0];
    B -- No --> D{unitsConsumed <= LIMIT_TIER1 (50)?};
    D -- Yes --> E[billTier1 = unitsConsumed * RATE_TIER1];
    D -- No --> F[billTier1 = LIMIT_TIER1 * RATE_TIER1];
    F --> G{unitsConsumed <= LIMIT_TIER2 (100)?};
    E --> K[electricityBill = billTier1 + billTier2 + billTier3 + billTier4];
    G -- Yes --> H[billTier2 = (unitsConsumed - LIMIT_TIER1) * RATE_TIER2];
    G -- No --> I[billTier2 = (LIMIT_TIER2 - LIMIT_TIER1) * RATE_TIER2];
    I --> J{unitsConsumed <= LIMIT_TIER3 (150)?};
    H --> K;
    J -- Yes --> L[billTier3 = (unitsConsumed - LIMIT_TIER2) * RATE_TIER3];
    J -- No --> M[billTier3 = (LIMIT_TIER3 - LIMIT_TIER2) * RATE_TIER3];
    M --> N[billTier4 = (unitsConsumed - LIMIT_TIER3) * RATE_TIER4];
    L --> K;
    N --> K;
    K --> O[Display electricityBill];
    C --> O;
    O --> P[End];
    %% Node Key:
    %% A: Start
    %% B: unitsConsumed <= 0
    %% C: bill = 0
    %% D: unitsConsumed <= 50
    %% E: calc tier 1 (units <= 50)
    %% F: calc tier 1 (units > 50)
    %% G: unitsConsumed <= 100
    %% H: calc tier 2 (units <= 100)
    %% I: calc tier 2 (units > 100)
    %% J: unitsConsumed <= 150
    %% L: calc tier 3 (units <= 150)
    %% M: calc tier 3 (units > 150)
    %% N: calc tier 4
    %% K: sum bills
    %% O: Display
    %% P: End


Nodes (N): A, B, C, D, E, F, G, H, I, J, L, M, N, K, O, P (16 nodes)
Edges (E):
1. A->B
2. B->C
3. B->D
4. D->E
5. D->F
6. E->K
7. F->G
8. G->H
9. G->I
10. H->K
11. I->J
12. J->L
13. J->M
14. L->K
15. M->N
16. N->K
17. K->O
18. C->O
19. O->P
(19 edges)

Predicate Nodes (P): B, D, G, J (4 predicate nodes)

### c) Cyclomatic Complexity (V(G))

Cyclomatic Complexity can be calculated using three formulas:
1.  V(G) = E - N + 2P (where P is the number of connected components, usually 1 for a single program/CFG)
    V(G) = E - N + 2
    V(G) = 19 - 16 + 2 = 3 + 2 = 5

2.  V(G) = P + 1 (where P is the number of predicate nodes/decision points)
    Predicate nodes are B, D, G, J. So, P = 4.
    V(G) = 4 + 1 = 5

3.  V(G) = Number of regions in the planar graph.
    By visual inspection of the CFG:
    Region 1: Outside the graph
    Region 2: B-D-E-K-O-C-B
    Region 3: D-F-G-H-K-E-D
    Region 4: G-I-J-L-K-H-G
    Region 5: J-M-N-K-L-J
    V(G) = 5

All methods yield **Cyclomatic Complexity V(G) = 5**. This means there are 5 independent paths through the code.

### d) Independent Paths

Based on V(G) = 5, we need to identify 5 independent paths.

1.  **Path 1 (units <= 0):**
    A -> B (Yes) -> C -> O -> P
    (Nodes: A, B, C, O, P)
    *Test Case: unitsConsumed = -5*

2.  **Path 2 (0 < units <= 50):**
    A -> B (No) -> D (Yes) -> E -> K -> O -> P
    (Nodes: A, B, D, E, K, O, P)
    *Test Case: unitsConsumed = 30*

3.  **Path 3 (50 < units <= 100):**
    A -> B (No) -> D (No) -> F -> G (Yes) -> H -> K -> O -> P
    (Nodes: A, B, D, F, G, H, K, O, P)
    *Test Case: unitsConsumed = 75*

4.  **Path 4 (100 < units <= 150):**
    A -> B (No) -> D (No) -> F -> G (No) -> I -> J (Yes) -> L -> K -> O -> P
    (Nodes: A, B, D, F, G, I, J, L, K, O, P)
    *Test Case: unitsConsumed = 125*

5.  **Path 5 (units > 150):**
    A -> B (No) -> D (No) -> F -> G (No) -> I -> J (No) -> M -> N -> K -> O -> P
    (Nodes: A, B, D, F, G, I, J, M, N, K, O, P)
    *Test Case: unitsConsumed = 200*

---

## Question 6: Function Point Metric Calculation

Given Information:
*   Number of external inputs (EIs) = 20, Complexity Weighting Factor = 3
*   Number of external output (EOs) = 30, Complexity Weighting Factor = 5
*   Number of external inquiries (EQs) = 23, Complexity Weighting Factor = 3
*   Number of files (ILF - Internal Logical Files) = 09, Complexity Weighting Factor = 10
*   Number of external interfaces (EIF) = 03, Complexity Weighting Factor = 7

Value Adjustment Factors (VAFs) - Total 14 factors:
*   Four factors: "Not Influential/Important"
*   Four factors: "Significant"
*   Remaining six factors (14 - 4 - 4 = 6): "Average"

Let's assume the standard scale for VAF ratings (0-5):
*   Not Influential/Important = 1 (Slight influence, as "No Influence" would be 0)
*   Average = 3 (Moderate influence)
*   Significant = 4 (Significant influence)

### 1) Total Unadjusted Function Points (UFP) / Count Total

UFP is calculated by summing the product of the count of each function type and its complexity weighting factor.

*   UFP_EI = Number of EIs * Weight_EI = 20 * 3 = 60
*   UFP_EO = Number of EOs * Weight_EO = 30 * 5 = 150
*   UFP_EQ = Number of EQs * Weight_EQ = 23 * 3 = 69
*   UFP_ILF = Number of ILFs * Weight_ILF = 9 * 10 = 90
*   UFP_EIF = Number of EIFs * Weight_EIF = 3 * 7 = 21

**Total Unadjusted Function Points (UFP)** = UFP_EI + UFP_EO + UFP_EQ + UFP_ILF + UFP_EIF
UFP = 60 + 150 + 69 + 90 + 21
**UFP = 390**

### 2) Cumulative Adjustment Factor (CAF)

The CAF (also referred to as Value Adjustment Factor - VAF in some contexts, but here VAF refers to the individual 14 factors) is calculated based on the sum of ratings for the 14 General System Characteristics (GSCs), often called Value Adjustment Factors.

Let DI be the sum of all 14 VAF ratings (Degree of Influence).
*   4 factors * "Not Influential/Important" (rating 1) = 4 * 1 = 4
*   4 factors * "Significant" (rating 4) = 4 * 4 = 16
*   6 factors * "Average" (rating 3) = 6 * 3 = 18

Sum of ratings (DI) = 4 + 16 + 18 = 38

The formula for CAF is:
CAF = 0.65 + (0.01 * DI)
CAF = 0.65 + (0.01 * 38)
CAF = 0.65 + 0.38
**CAF = 1.03**

### 3) Total Adjusted Function Points (AFP)

The Total Adjusted Function Points (AFP) is calculated by multiplying the UFP by the CAF.

AFP = UFP * CAF
AFP = 390 * 1.03
**AFP = 401.7**

Since Function Points are typically expressed as whole numbers, AFP can be rounded to **402**.

**Summary of Results:**
1.  **Total Unadjusted Function Points (UFP) = 390**
2.  **Cumulative Adjustment Factor (CAF) = 1.03**
3.  **Total Adjusted Function Points (AFP) = 401.7 (or 402 rounded)**
