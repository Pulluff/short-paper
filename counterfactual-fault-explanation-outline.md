# Draft outline for explaining motor overheating

## 1. Introduction

- When a motor has both weakened magnets and excess friction, which fault would have to disappear to keep the winding below 90 °C? Mujić and Wotawa’s simulated motor gives a case where both faults matter, but removing them has different consequences. [Mujić and Wotawa, §5.2 and Table 2](sources/mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=13)
- Reiter defines a diagnosis as a minimal set of faulty components consistent with the observations and system description. Even when we know which faults are present, we can still ask what each contributed to a particular symptom. [Reiter, Definition 2.4, p. 63](sources/reiter-1987/reiter.pdf#page=7)

## 2. Structural models and actual causation

- An intervention changes one mechanism and lets its consequences unfold under the same background conditions. For Halpern and Pearl, both the candidate cause and the outcome must have occurred. The outcome must depend on the candidate under a suitable contingency, and the candidate must contain no redundant parts. [Halpern and Pearl, §2](sources/halpern-pearl-2005/actcaus.pdf#page=5) · [Definition 3.1](sources/halpern-pearl-2005/actcaus.pdf#page=10)
- Why allow a contingency? If either of two matches is sufficient to start a fire, removing one still leaves a fire. Holding the second match unlit reveals the difference the first one makes. This is why failure to prevent an event by one removal alone cannot settle every causal question. [Halpern and Pearl, Example 3.2](sources/halpern-pearl-2005/actcaus.pdf#page=13)

## 3. Counterfactual fault removal in a dynamic system

- Mujić and Wotawa switch off one fault at a time while keeping the other fault, starting state, task and load fixed. The controller recomputes its voltage command as the simulated motor responds. [§3.3, Eqs. (11)–(13)](sources/mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=7)
- To assess **severity**, ask whether removal lowered the peak by more than 5 °C, the authors’ criterion for a contribution. To assess **necessity**, ask whether removal kept the winding below 90 °C when the factual run reached that threshold. [§4.2, Eqs. (18)–(19)](sources/mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=10)

## 4. Analysis of the published DC motor case

- **Establish the baseline.** The winding peaked at 105.70 °C with both faults active and at 81.30 °C with both removed. The two single-fault removals tell us what each fault contributed. [Mujić and Wotawa, Table 2](sources/mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=13)
- **Remove partial demagnetization.** The peak fell by 9.18 °C to 96.52 °C. The fault made the winding hotter, and excess friction alone still took it past 90 °C. [Table 2](sources/mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=13)
- **Remove excess viscous friction.** The peak fell by 17.19 °C to 88.51 °C, preventing overheating. Figure 3 shows the physical connection. The motor drew less current to follow the same task once the extra friction was removed. [Fig. 3](sources/mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=12) · [Table 2](sources/mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=13)

## 5. Discussion and limitations

- **Thought experiment for this paper.** Suppose the threshold were 100 °C. The factual peak still qualifies, while both single-removal peaks fall below it. Either removal would now prevent the event. Changing the definition of overheating changes the answer even when the trajectories stay the same. [Published peaks in Table 2](sources/mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=13)
- **How far does the 90 °C result travel?** The authors recovered the friction attribution in 84 of 100 runs with varied model parameters. They also started from the true simulated state. On a physical motor, that state would need to be estimated from noisy measurements. [Mujić and Wotawa, §§5.2–6](sources/mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=12)

## 6. Conclusion

- Answer the opening question directly. Under the published operating conditions, removing excess friction would have prevented the 90 °C event. Removing partial demagnetization would have made the same event less severe. The distinction depends on both the change in peak temperature and where that peak falls relative to the chosen limit. [Mujić and Wotawa, Table 2](sources/mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=13)
