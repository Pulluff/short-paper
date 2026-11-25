# Writing roadmap for a six-page paper on counterfactual fault explanation

## Scope and central question

This is a **theoretical, literature-based paper**. It explains and evaluates published methods and interprets results reported by Mujić and Wotawa. It does not require a motor, a simulation, or new experimental data. Any numerical example below is an analytical calculation using values from their paper.

**Working title:** Why Did the Motor Overheat? A Counterfactual Analysis of Two Simultaneous Faults

**Research question:** When two faults are present, how can counterfactual reasoning distinguish a fault that was necessary for overheating from one that increased its severity?

**Working thesis:** In Mujić and Wotawa's simulated case, both partial demagnetization and excess friction increased the peak winding temperature. At the authors' 90 °C threshold, removing friction prevented overheating, whereas removing demagnetization reduced its severity without preventing the event. The conclusion depends on the specified outcome, threshold, operating conditions, and causal model.

## The published case to analyze

Mujić and Wotawa simulate a DC motor with two faults, partial demagnetization and increased viscous friction. They compare the factual trajectory with counterfactual trajectories in which a fault is removed. The initial state, task, and load are held fixed. The controller responds to the motor's behavior in each trajectory. These are **the authors' simulations**.

| Fault removed | Peak winding temperature | Crosses 90 °C? |
|---|---:|:---:|
| None | 105.70 °C | Yes |
| Partial demagnetization | 96.52 °C | Yes |
| Increased viscous friction | 88.51 °C | No |
| Both | 81.30 °C | No |

Source: [Mujić and Wotawa (2026), Table 2](https://drops.dagstuhl.de/storage/01oasics/oasics-vol148-dx2026/OASIcs.DX.2026.16/OASIcs.DX.2026.16.pdf#page=13).

Two calculations make the distinction precise. If `P` is the factual peak and `Q` is the peak after removing one fault, the reduction in peak temperature is `P − Q`. Removal prevents an event defined by threshold `θ` when `Q < θ ≤ P`. Removing demagnetization reduces the peak by 9.18 °C. Removing excess friction reduces it by 17.19 °C. Only the latter removal prevents the authors' 90 °C event.

For your **own theoretical analysis**, ask what the same published peaks imply for a *hypothetical* 100 °C threshold. Either single-fault removal would then prevent the event. Label 100 °C clearly as your thought experiment. This shows how a causal conclusion changes with the event being explained without claiming to have run a new experiment.

## Sources and reading priorities

1. **Halpern and Pearl (2005), *Causes and Explanations: A Structural-Model Approach. Part I: Causes*.** Read §§2–3, especially Definition 3.1 and Example 3.2. Use it to explain structural causal models, interventions, actual causation, and why a direct single-removal test can miss a cause when another fault could also produce the event. [Full text](https://www.cs.cornell.edu/home/halpern/papers/actcaus.pdf)
2. **Mujić and Wotawa (2026), *Counterfactual Fault Responsibility in a Dynamic Structural Causal Model of a DC Motor*.** Read §3.3 for the method, §§4.2 and 5.2 for the overheating case, and §6 for limitations. Use Table 2 as the central evidence. [Full text](https://drops.dagstuhl.de/storage/01oasics/oasics-vol148-dx2026/OASIcs.DX.2026.16/OASIcs.DX.2026.16.pdf)
3. **Recommended addition: Reiter (1987), *A Theory of Diagnosis from First Principles*.** Use a short passage in the introduction to establish the diagnostic task of finding fault hypotheses consistent with abnormal observations. That sets up the question of which fault explains a particular symptom. [Publication page](https://doi.org/10.1016/0004-3702(87)90062-2)
4. **Optional: Chockler and Halpern (2004), *Responsibility and Blame: A Structural-Model Approach*.** Read it only if you plan to discuss the formal *degree of responsibility*. Its measure concerns the smallest contingency needed to make a cause critical. The motor paper's score measures the change in a chosen symptom after fault removal, so define which meaning you use. [Full text](https://www.cs.cmu.edu/afs/cs/project/jair/pub/volume22/chockler04a.pdf)

The two assigned papers are enough for the central argument. Reiter adds a concise foundation for the diagnosis context. The optional fourth paper is useful only if the formal meaning of responsibility becomes part of your argument.

## Six-page structure

The budget assumes the references and any required short abstract count toward six pages. If your course excludes references from the limit, give the extra space to the discussion.

| Section | Pages | Purpose |
|---|---:|---|
| 1. Introduction and abstract, if required | 0.75 | Present the two-fault puzzle, the diagnostic setting, and the research question. |
| 2. Actual causation | 1.00 | Explain context, interventions, counterfactual dependence, contingencies, and minimality in plain language. |
| 3. Counterfactual fault removal | 0.75 | Explain the published method, what changes between trajectories, and the difference between temperature reduction and event prevention. |
| 4. Analysis of the overheating case | 1.75 | Present a compact version of Table 2 and interpret each single-fault removal. Attribute all results to Mujić and Wotawa. |
| 5. Theoretical discussion and limitations | 1.00 | Develop the hypothetical 100 °C threshold and discuss dependence on model accuracy, event thresholds, and simulated starting states. |
| 6. Conclusion | 0.25 | Answer the research question for this case and state the scope of the conclusion. |
| References | 0.50 | List only sources actually cited. |
| **Total** | **6.00** | |

## Writing sequence

1. Read Table 2 and write one sentence about the temperature change and one about event prevention for each intervention.
2. Draft the case analysis first. Then use Halpern and Pearl to explain the causal reasoning behind it.
3. Write your own discussion of the hypothetical 100 °C threshold. Add the limitations reported by Mujić and Wotawa. Their friction attribution held in 84 of 100 repetitions with varied model parameters, and their counterfactual runs used the true simulated starting state.
4. Write the introduction, conclusion, and abstract last. Check every number against Table 2 and make clear which claims are reported results and which are your deductions.
5. Cut the motor's detailed equations and the full fault catalogue first if the draft exceeds six pages. Preserve the explanation of the counterfactual method, the case analysis, and your theoretical discussion.
