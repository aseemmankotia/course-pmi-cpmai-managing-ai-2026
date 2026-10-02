## Chapter 2: Framing the Business Problem and the Seven Patterns of AI — Practice Questions

**Q1.** A bank wants to detect unusual transactions that deviate from a customer's normal spending behavior in real time to flag potential fraud. Which of the Seven Patterns of AI BEST fits this business problem?

A) Hyperpersonalization
B) Patterns and Anomalies
C) Goal-Driven Systems
D) Conversational/Human Interaction

<details>
<summary>Answer</summary>

**Correct: B**

Detecting deviations from established behavioral baselines is the defining use case of the Patterns and Anomalies pattern, which covers fraud detection, network intrusion, and quality control.

**Why the others are wrong:**
- Hyperpersonalization tailors content/offers to individuals, it doesn't detect deviation from a norm.
- Goal-Driven Systems optimize toward a defined objective (e.g., resource allocation), not deviation detection.
- Conversational/Human Interaction covers chatbots and NLP interfaces, unrelated to transaction monitoring.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A retailer is building a system that answers customer questions via a website chat widget, using natural language to understand intent and respond conversationally. Which pattern applies?

A) Recognition Patterns
B) Autonomous Systems
C) Conversational/Human Interaction
D) Predictive Analytics and Decision Support

<details>
<summary>Answer</summary>

**Correct: C**

Systems that use NLP/NLU to interact with humans through text or voice—chatbots, virtual assistants—map directly to the Conversational/Human Interaction pattern.

**Why the others are wrong:**
- Recognition Patterns applies to identifying objects, faces, or speech-to-text conversion, not conversational dialogue management.
- Autonomous Systems act independently in physical or digital environments without ongoing human dialogue.
- Predictive Analytics and Decision Support forecasts outcomes; it doesn't govern conversational exchange.

</details>

---

**Q3.** An e-commerce company wants to show each shopper individually tailored product recommendations and dynamically adjusted pricing based on their browsing history. Which pattern is this?

A) Hyperpersonalization
B) Goal-Driven Systems
C) Patterns and Anomalies
D) Recognition Patterns

<details>
<summary>Answer</summary>

**Correct: A**

Tailoring content, offers, or experiences to the individual based on their data is the core definition of Hyperpersonalization.

**Why the others are wrong:**
- Goal-Driven Systems optimize toward a fixed objective like routing or scheduling, not individualized content delivery.
- Patterns and Anomalies focuses on finding deviations from the norm, not customizing experiences.
- Recognition Patterns identifies entities (images, speech, text) rather than personalizing content.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A manufacturer wants a delivery drone that can navigate, avoid obstacles, and make routing decisions in real time without a human operator. Which pattern of AI does this project belong to?

A) Predictive Analytics and Decision Support
B) Conversational/Human Interaction
C) Autonomous Systems
D) Hyperpersonalization

<details>
<summary>Answer</summary>

**Correct: C**

Systems that sense, decide, and act independently in an environment—self-driving vehicles, drones, robots—are classified under Autonomous Systems.

**Why the others are wrong:**
- Predictive Analytics and Decision Support forecasts future outcomes to support human decisions; it doesn't act independently.
- Conversational/Human Interaction requires an ongoing dialogue loop with a person, which a drone doesn't need.
- Hyperpersonalization is about tailoring content to individuals, irrelevant to physical navigation.

</details>

---

**Q5.** An airline wants to forecast which aircraft components are likely to fail in the next 30 days so maintenance can be scheduled proactively. Which pattern BEST matches this need?

A) Recognition Patterns
B) Goal-Driven Systems
C) Patterns and Anomalies
D) Predictive Analytics and Decision Support

<details>
<summary>Answer</summary>

**Correct: D**

Forecasting a future outcome (component failure) to support a human decision (scheduling maintenance) is the textbook definition of Predictive Analytics and Decision Support.

**Why the others are wrong:**
- Recognition Patterns identifies existing objects/entities in data (e.g., visual defects), not future states.
- Goal-Driven Systems optimizes toward an objective like minimizing cost, not forecasting a probability of failure.
- Patterns and Anomalies is commonly confused with predictive maintenance, but it detects existing abnormal behavior rather than forecasting a future event—students often pick this incorrectly.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** During the CPMAI Business Understanding phase, which deliverable is REQUIRED before a project can proceed to Data Understanding?

A) A trained baseline model with accuracy metrics
B) A documented business problem statement with defined success criteria
C) A fully labeled training dataset
D) A deployed pilot in a production environment

<details>
<summary>Answer</summary>

**Correct: B**

CPMAI's Business Understanding phase requires a clearly documented business problem, objectives, and measurable success criteria (e.g., an AI project charter) before any data or modeling work begins.

**Why the others are wrong:**
- A trained model belongs to the Modeling phase, far later in the CPMAI lifecycle.
- A labeled dataset is a Data Preparation phase deliverable, not Business Understanding.
- A deployed pilot occurs in the Operationalize/Deployment phase, the final iterative stage.

</details>

---

**Q7.** A project team conducted stakeholder interviews but got conflicting descriptions of the current manual process. What is the BEST next step to validate the true business need before selecting an AI pattern?

A) Conduct SME walkthroughs and process observation to reconcile the conflicting accounts
B) Select the pattern preferred by the most senior stakeholder
C) Skip validation and proceed directly to data collection
D) Choose the pattern with the lowest implementation cost

<details>
<summary>Answer</summary>

**Correct: A**

When stakeholder accounts conflict, CPMAI practice calls for direct validation with subject matter experts—process walkthroughs, shadowing, or observation—to establish ground truth before mapping the problem to a pattern.

**Why the others are wrong:**
- Deferring to seniority ignores factual process reality and risks mapping to the wrong pattern.
- Skipping validation violates the Business Understanding phase requirement to confirm the problem before proceeding.
- Cost is a feasibility factor evaluated later, not a substitute for validating what the actual process/problem is.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** How does a Goal-Driven Systems pattern fundamentally differ from an Autonomous Systems pattern?

A) Goal-Driven Systems optimize a defined objective function within constraints; Autonomous Systems sense and act independently in an environment, which may include pursuing goals
B) Goal-Driven Systems always require human approval before acting; Autonomous Systems never do
C) Goal-Driven Systems only apply to physical robots; Autonomous Systems only apply to software
D) There is no meaningful difference; the terms are interchangeable in CPMAI

<details>
<summary>Answer</summary>

**Correct: A**

Goal-Driven Systems (e.g., route optimization, resource allocation via reinforcement learning) are defined by optimizing toward an objective function, whereas Autonomous Systems are defined by independent sensing and acting in an environment—an autonomous system may itself pursue goals, but the classification hinges on independent action, not optimization alone.

**Why the others are wrong:**
- Human approval requirements are not the distinguishing criterion in the CPMAI pattern definitions.
- Both patterns can apply to physical or software-based systems; the split is not physical vs. software.
- The two are distinct patterns in the Seven Patterns of AI framework and are tested separately on the exam.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

