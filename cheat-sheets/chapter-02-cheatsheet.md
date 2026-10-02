## Chapter 2 Cheat Sheet: Seven Patterns of AI & Business Problem Framing

### The Seven Patterns of AI (memorize order for exam)
| # | Pattern | Core Definition | Classic Example |
|---|---------|------------------|------------------|
|1| Hyperpersonalization | Tailors content/offers to the individual | Recommendation engines, dynamic pricing |
|2| Autonomous Systems | Senses, decides, acts independently in environment | Self-driving cars, drones, robots |
|3| Predictive Analytics & Decision Support | Forecasts future outcome for human decision | Predictive maintenance, demand forecasting |
|4| Conversational/Human Interaction | NLP/NLU-driven dialogue with humans | Chatbots, voice assistants |
|5| Patterns and Anomalies | Detects deviation from established norm | Fraud detection, intrusion detection |
|6| Recognition Patterns | Identifies/classifies entities in data | Facial recognition, OCR, speech-to-text |
|7| Goal-Driven Systems | Optimizes toward defined objective function | Route optimization, resource allocation |

### Frequently Confused Pairs
| Pattern A | Pattern B | Key Differentiator |
|-----------|-----------|---------------------|
| Patterns and Anomalies | Predictive Analytics | Anomalies = deviation happening NOW; Predictive = forecasts FUTURE event |
| Autonomous Systems | Goal-Driven Systems | Autonomous = independent action in environment; Goal-Driven = optimizing an objective function (may lack independent physical action) |
| Recognition Patterns | Conversational/Human Interaction | Recognition = classify/identify entity; Conversational = sustain a dialogue loop |

### CPMAI Business Understanding Phase — Deliverables Checklist
- Documented business problem statement
- Defined business objectives & measurable success criteria
- AI project charter
- Stakeholder map
- Initial feasibility/ROI assessment
- Mapped candidate AI Pattern(s)

*Exam Note:* No data collection or modeling should begin before these deliverables are validated with SMEs.

### Stakeholder Interview & SME Validation Techniques
| Technique | When to Use |
|-----------|--------------|
| Open-ended discovery interviews | Early-stage problem framing |
| 5 Whys | Drilling to root cause of a process pain point |
| Process walkthroughs / shadowing | Reconciling conflicting stakeholder accounts |
| JAD (Joint Application Design) sessions | Aligning multiple stakeholders on requirements |
| SME sign-off / validation review | Confirming problem statement accuracy before pattern selection |

### Persona & Use Case Development
- **Persona:** WHO — representative user profile (goals, frustrations, context)
- **Use Case:** WHAT/HOW — specific scenario of persona interacting with proposed AI solution
- Both must trace back to a validated business problem and map to one (or more) of the Seven Patterns.

### Common Exam Traps
1. Picking "Patterns and Anomalies" for predictive maintenance scenarios (should be Predictive Analytics if forecasting a *future* failure).
2. Assuming Autonomous Systems only applies to physical robots — it can apply to fully independent software agents too.
3. Treating personas and use cases as interchangeable — the exam tests the distinction explicitly.
4. Believing modeling can start once stakeholder interviews are done — Business Understanding deliverables must be SME-validated first.
