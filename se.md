# Software Engineering Exam - Scenario-Based Questions & Answers

Here are 5 scenario-based questions designed according to the provided topics, each worth 10 marks. Detailed answers are provided below each question.

---

## Question 1 (SDLC Models & Comparison - 10 Marks)

**Scenario:** A large financial institution, "SecureBank," wants to develop a new online banking platform. The requirements are well-understood, and the scope is unlikely to change significantly. However, they also want to incorporate some modern features using newer technologies, which might require iterative feedback. The management team is debating between using a traditional Waterfall model and adopting an Agile approach. They have also heard about the Unified Process.

**Task:**
a) Briefly explain the core phases of the Waterfall Model. Why might SecureBank consider it suitable given their well-understood requirements? (3 Marks)
b) Explain the core principles of Agile methods. How does the delivery of working software differ between Waterfall and Agile? Why might Agile be considered despite stable requirements? (5 Marks)
c) Briefly describe the phases of the Unified Process. Could it offer a compromise? (Include a link to a diagram illustrating the phases). (2 Marks)

**Answer:**

**a) Waterfall Model:**
The Waterfall Model is a sequential software development process where progress flows steadily downwards (like a waterfall) through distinct phases. The main phases are:
1.  **Requirements Analysis:** Gathering and documenting all system requirements.
2.  **System Design:** Defining the hardware and software architecture, data structures, interfaces, etc.
3.  **Implementation:** Writing the code based on the design specifications.
4.  **Testing:** Verifying and validating the implemented system against the requirements.
5.  **Deployment:** Releasing the software to the customer/market.
6.  **Maintenance:** Making changes post-release to fix bugs, improve performance, or add minor enhancements.

*Suitability for SecureBank:* SecureBank might consider Waterfall suitable because their core requirements for an online banking platform are well-understood and stable. Waterfall excels in projects where scope is fixed, documentation is crucial (important for financial institutions), and a structured, linear approach is preferred. Each phase is completed and signed off before the next begins, providing clear milestones and control.

**b) Agile Methods & Delivery Comparison:**
Agile methods represent an iterative and incremental approach to software development. Core principles (based on the Agile Manifesto) include:
*   Individuals and interactions over processes and tools.
*   Working software over comprehensive documentation.
*   Customer collaboration over contract negotiation.
*   Responding to change over following a plan.

*Delivery Difference:*
*   **Waterfall:** Delivers the complete, working software product only at the *end* of the entire project lifecycle (after the Testing phase). There's typically one major delivery.
*   **Agile:** Delivers working software in *small, frequent increments* (iterations or sprints, often every 2-4 weeks). Each increment contains a subset of functional features, allowing for early and continuous delivery and feedback.

*Why Agile Might Be Considered:* Even with stable core requirements, SecureBank wants to incorporate *modern features using newer technologies*. Agile's iterative nature allows the team to build and test these features incrementally, gather feedback early (perhaps from internal stakeholders or pilot users), and adapt the implementation based on that feedback or technological challenges. This reduces the risk associated with integrating new technologies compared to building everything and testing only at the end (Waterfall).

**c) Unified Process (UP):**
The Unified Process is an iterative and incremental framework, adaptable and use-case driven. It consists of four main phases, each potentially containing multiple iterations:
1.  **Inception:** Define the project scope, business case, and initial architecture. Assess feasibility.
2.  **Elaboration:** Analyze the problem domain, establish a robust architectural baseline, develop the project plan, and mitigate high-risk elements. Most requirements are detailed here.
3.  **Construction:** Build the software iteratively, developing the remaining use cases and features, leading to the first operational version. Heavy coding and testing occur here.
4.  **Transition:** Deploy the software to end-users. Includes beta testing, user training, and final adjustments based on feedback.

*Diagram Link:* [Example Unified Process Phases Diagram](https://upload.wikimedia.org/wikipedia/commons/thumb/1/16/Unified_Process_Phases_and_Disciplines.svg/800px-Unified_Process_Phases_and_Disciplines.svg.png)

*Compromise Potential:* Yes, the Unified Process could offer a compromise. It provides more structure and documentation emphasis than some Agile methods (appealing given the financial context) but is still iterative and incremental (allowing for handling the newer features and gathering feedback like Agile). It focuses on addressing risks early (Elaboration phase), which is crucial for complex systems.

---

## Question 2 (Requirements Engineering & Feasibility - 10 Marks)

**Scenario:** A startup, "FitTrack," has a concept for a mobile application that uses smartphone sensors and user input to provide personalized workout plans and dietary recommendations. They have a basic idea but need to formalize it before seeking funding and starting development.

**Task:**
a) Define Requirement Engineering and list its key phases. (3 Marks)
b) Explain the techniques FitTrack could use for Requirement Elicitation and Analysis to understand user needs and system functionalities better. (4 Marks)
c) Describe the purpose of a Feasibility Study in this context and list its key advantages for FitTrack. (3 Marks)

**Answer:**

**a) Requirement Engineering:**
Requirement Engineering (RE) is the process of defining, documenting, and maintaining requirements for a software system. It acts as a bridge between the stakeholders' needs and the system's design and implementation. Its goal is to ensure the final system meets user expectations and business objectives.

Key Phases of Requirement Engineering:
1.  **Elicitation:** Gathering requirements from stakeholders (users, customers, domain experts).
2.  **Analysis:** Refining, structuring, and modeling requirements to resolve conflicts, ambiguities, and incompleteness. Checking for consistency.
3.  **Specification:** Documenting the agreed-upon requirements clearly and unambiguously (e.g., in a Software Requirements Specification - SRS document).
4.  **Validation:** Ensuring the specified requirements accurately reflect stakeholder needs and are feasible.
5.  **Management:** Handling changes to requirements throughout the project lifecycle.

**b) Requirement Elicitation and Analysis Techniques for FitTrack:**
*   **Elicitation Techniques:**
    *   **Interviews:** Conduct structured or unstructured interviews with potential users (gym-goers, fitness enthusiasts, dieticians) and stakeholders (investors, fitness trainers) to understand their needs, pain points, and desired features.
    *   **Surveys/Questionnaires:** Distribute surveys to a wider audience to gather quantitative data on preferred features, existing app usage, and demographic information.
    *   **Prototyping:** Develop simple mockups or interactive prototypes of the app interface. Show these to potential users to get feedback on usability and features early on.
    *   **Use Cases/User Stories:** Define specific scenarios of how different users (e.g., beginner athlete, nutritionist) would interact with the app to achieve their goals (e.g., "As a user, I want to log my daily food intake to track calories").
    *   **Competitive Analysis:** Analyze existing fitness and diet apps to identify common features, gaps in the market, and potential differentiators for FitTrack.

*   **Analysis Techniques:**
    *   **Requirements Classification:** Group requirements into categories (e.g., functional, non-functional, performance, security).
    *   **Conceptual Modeling:** Create models like Data Flow Diagrams (DFDs) or Entity-Relationship Diagrams (ERDs) to visualize data processing and relationships. Use UML diagrams (like Use Case diagrams, Class diagrams) to model system structure and behavior.
    *   **Negotiation:** Discuss conflicting requirements among stakeholders to reach a consensus. Prioritize requirements (e.g., using MoSCoW - Must have, Should have, Could have, Won't have).

**c) Feasibility Study & Advantages for FitTrack:**
A Feasibility Study is an assessment conducted early in the project (often during Inception or before Elicitation) to determine if the proposed project is viable and worth pursuing. It evaluates the project from different perspectives. For FitTrack, it would assess if developing the personalized fitness app is practical and makes business sense.

Key Areas of Feasibility:
1.  **Technical Feasibility:** Can the app be built with current technology? Are the required smartphone sensors accurate enough? Does the team have the technical expertise?
2.  **Economic Feasibility:** Will the project generate benefits that outweigh the costs? Can FitTrack secure funding based on the potential ROI? What are the development and operational costs?
3.  **Legal Feasibility:** Does the app comply with data privacy regulations (like GDPR or HIPAA if health data is sensitive)? Are there any patent or licensing issues?
4.  **Operational Feasibility:** Will the app integrate with users' lifestyles? Can FitTrack support the app post-launch (customer service, updates)?
5.  **Schedule Feasibility:** Can the app be developed within a reasonable timeframe to meet market opportunities?

*Advantages for FitTrack:*
*   **Risk Reduction:** Identifies potential problems early, allowing FitTrack to mitigate them or decide not to proceed, saving resources.
*   **Informed Decision-Making:** Provides management and potential investors with solid data to decide whether to commit to the project.
*   **Resource Optimization:** Helps determine the required resources (financial, technical, human) more accurately.
*   **Improved Project Focus:** Narrows down the project scope to what is achievable and valuable.
*   **Increased Success Probability:** By addressing potential roadblocks upfront, it increases the chances of the project succeeding if undertaken.

---

## Question 3 (Testing Techniques & Complexity - 10 Marks)

**Scenario:** A software team is developing a critical module for an avionics system that calculates landing trajectory based on various inputs (altitude, speed, wind). Due to the critical nature, rigorous testing is required.

**Task:**
a) Explain the fundamental difference between Black Box Testing and White Box Testing. Which approach would be essential for this avionics module, and why? (3 Marks)
b) Consider the following pseudo-code snippet for a function within the module. Draw the Control Flow Graph (CFG) and calculate its Cyclomatic Complexity (V(G)). Explain what this complexity value indicates. (4 Marks)

```pseudocode
1. FUNCTION CalculateTrajectory(altitude, speed, wind)
2.   IF altitude < 1000 THEN
3.     IF speed > 200 THEN
4.       trajectory = "Abort Landing"
5.     ELSE
6.       trajectory = "Adjust Approach"
7.     ENDIF
8.   ELSE
9.     IF wind > 30 THEN
10.      trajectory = "Monitor Wind Shear"
11.    ELSE
12.      trajectory = "Standard Approach"
13.    ENDIF
14.  ENDIF
15.  RETURN trajectory
16. END FUNCTION
```

c) Briefly explain the relationship between Unit Testing and Integration Testing in the context of developing this module. Would a Top-Down or Bottom-Up integration strategy be more suitable? Justify your choice. (3 Marks)

**Answer:**

**a) Black Box vs. White Box Testing:**
*   **Black Box Testing:** This technique focuses on testing the *functionality* of the software without looking at its internal code structure or implementation details. Testers treat the software as a "black box," providing inputs and verifying the outputs against the specified requirements. Techniques include equivalence partitioning, boundary value analysis, and decision table testing.
*   **White Box Testing:** This technique focuses on testing the *internal structure*, design, and code of the software. Testers have access to the source code and analyze control flow, data flow, and code coverage (e.g., statement, branch, path coverage). Techniques include statement coverage, branch coverage, path testing, and cyclomatic complexity analysis.

*Essential Approach for Avionics Module:* **Both** approaches are essential, but **White Box Testing** is particularly critical.
*   *Why White Box:* For safety-critical systems like avionics, it's not enough to know *that* it works for some inputs (Black Box); you need to ensure *how* it works internally is correct and robust. White Box testing allows verification of all logical paths, conditions, and branches within the code, ensuring there are no hidden flaws in the calculation logic that could lead to catastrophic failure. Code coverage metrics (from White Box testing) are often mandated by avionics standards (like DO-178C).
*   *Why Black Box is also needed:* Black Box testing is still necessary to validate that the module meets its specified functional requirements from an external perspective, ensuring it behaves correctly according to the overall system design and user expectations under various input conditions.

**b) Control Flow Graph (CFG) and Cyclomatic Complexity:**

*   **Control Flow Graph (CFG):**
    (Nodes represent processing blocks, edges represent control flow)

    ```mermaid
    graph TD
        N1[1] --> N2{2: altitude < 1000?};
        N2 -- True --> N3{3: speed > 200?};
        N2 -- False --> N8{9: wind > 30?};
        N3 -- True --> N4[4];
        N3 -- False --> N5[6];
        N4 --> N7[7: ENDIF];
        N5 --> N7;
        N7 --> N14[14: ENDIF];
        N8 -- True --> N9[10];
        N8 -- False --> N10[12];
        N9 --> N11[13: ENDIF];
        N10 --> N11;
        N11 --> N14;
        N14 --> N15[15];
        N15 --> N16((16: END));
    ```
    *(Note: Some CFG conventions merge sequential statements. Here, each decision/action block gets a node for clarity. Node 16 represents the exit point.)*

*   **Cyclomatic Complexity (V(G)):**
    V(G) measures the number of linearly independent paths through a program's source code. It indicates the complexity of the code's control flow.
    There are three ways to calculate it:
    1.  `V(G) = E - N + 2P` (Where E = number of edges, N = number of nodes, P = number of connected components, usually 1 for a single function)
        *   Nodes (N) = 13 (N1, N2, N3, N4, N5, N7, N8, N9, N10, N11, N14, N15, N16)
        *   Edges (E) = 15 (1->2, 2->3, 2->8, 3->4, 3->5, 4->7, 5->7, 7->14, 8->9, 8->10, 9->11, 10->11, 11->14, 14->15, 15->16)
        *   P = 1
        *   V(G) = 15 - 13 + 2 * 1 = 2 + 2 = 4
    2.  `V(G) = Number of Predicate Nodes (decisions) + 1`
        *   Predicate Nodes (nodes with more than one outgoing edge): N2, N3, N8
        *   V(G) = 3 + 1 = 4
    3.  `V(G) = Number of Regions` in the planar CFG graph.
        *   Counting the enclosed regions + the outer region = 3 + 1 = 4

    *Calculation Result:* V(G) = 4

    *Indication:* A Cyclomatic Complexity of 4 indicates moderate complexity. It suggests that there are 4 linearly independent paths through this function. To achieve full path coverage (a rigorous White Box testing goal), at least 4 distinct test cases would be needed to execute every possible path combination through the conditional logic. Higher complexity generally implies more difficult code to understand, test, and maintain, and a higher likelihood of defects.

**c) Unit Testing, Integration Testing, and Strategy:**
*   **Relationship:**
    *   **Unit Testing:** Focuses on testing individual components or functions (units) of the software in isolation. For the avionics module, `CalculateTrajectory` would be a unit. Unit tests verify that each small piece of code works correctly on its own, often using stubs or drivers to simulate dependencies.
    *   **Integration Testing:** Focuses on testing the interaction and communication *between* different units or modules after they have been integrated. For example, testing how the `CalculateTrajectory` module interacts with modules that provide altitude/speed/wind data, or modules that consume its output (e.g., display systems, autopilot control). It verifies that integrated components work together as expected. Unit testing precedes integration testing.

*   **Integration Strategy Choice:** **Bottom-Up** integration might be more suitable here.
    *   **Justification:** In Bottom-Up integration, the lowest-level units (like `CalculateTrajectory` and other calculation functions) are tested first (Unit Testing). Then, these tested units are progressively integrated with higher-level modules (e.g., modules that manage sensor input or control surfaces) and tested together. For a critical calculation module, ensuring the fundamental logic is correct *before* integrating it into the larger system is crucial. Bottom-Up allows for early verification of the core, critical algorithms in isolation and then as part of progressively larger subsystems. While Top-Down (testing high-level modules first using stubs for lower ones) can validate overall architecture early, it might delay finding critical bugs in the low-level calculation logic until later in the integration process. Given the safety-critical nature, verifying the base calculations thoroughly first (Bottom-Up) seems prudent.

---

## Question 4 (Software Estimation - 10 Marks)

**Scenario:** A project manager at "WebSolutions Inc." needs to estimate the effort required for developing a new Content Management System (CMS) for a client. Initial analysis suggests the system will have approximately:
*   5 complex external inputs (e.g., user registration form, article submission form)
*   10 average external outputs (e.g., displaying articles, user profiles)
*   8 average external inquiries (e.g., search function, category listing)
*   20 average internal logical files (e.g., user data table, article content table)
*   15 simple external interface files (e.g., connection to a payment gateway API)

The team primarily uses Java, and historical data is limited.

**Task:**
a) Explain the concept of Function Point (FP) Estimation. Using the counts provided and assuming standard complexity weighting factors (provide reasonable example weights if not given), calculate the Unadjusted Function Points (UFP). (6 Marks)
b) Explain the Basic COCOMO model. What key input does it primarily rely on, and what does it estimate? How could the manager use the FP result from part (a) to potentially feed into a COCOMO estimate? (4 Marks)

**Answer:**

**a) Function Point (FP) Estimation:**
Function Point Analysis (FPA) is a method used to measure the functional size of an information system based on the functions it provides to the user, independent of the technology used for implementation. It quantifies functionality from the user's perspective. The process involves:
1.  **Identifying Function Types:** Classifying system functions into five types:
    *   External Inputs (EI): Processing data/control information entering the system (e.g., forms).
    *   External Outputs (EO): Presenting data/control information leaving the system (e.g., reports, displays).
    *   External Inquiries (EQ): Input/output combinations requiring immediate retrieval (e.g., lookups, searches).
    *   Internal Logical Files (ILF): User-identifiable groups of logically related data maintained within the system boundary (e.g., database tables).
    *   External Interface Files (EIF): User-identifiable groups of data referenced by the system but maintained outside its boundary (e.g., data from other apps, APIs).
2.  **Assessing Complexity:** Determining the complexity (Simple, Average, Complex) for each identified function instance based on predefined criteria (e.g., number of data elements, referenced files).
3.  **Calculating Unadjusted Function Points (UFP):** Multiplying the count of each function type by its corresponding complexity weight and summing the results.
