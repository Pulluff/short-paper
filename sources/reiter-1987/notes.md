# A Theory of Diagnosis from First Principles

Raymond Reiter (1987). *Artificial Intelligence* 32(1), 57–95. LaTeX key `reiter1987`. [DOI](https://doi.org/10.1016/0004-3702%2887%2990062-2) · [Radboud University PDF](https://www.cs.ru.nl/~peterl/teaching/KeR/reiter.pdf)

## Summary

Reiter starts with a system whose observed behavior conflicts with the assumption that all components work correctly. A diagnosis identifies a set of components that can be assumed abnormal, with all remaining components healthy, consistently with the design and observations. The set must be minimal under inclusion. Several diagnoses can fit the same observation, and some may involve more faults than others. [§1, pp. 57–58](reiter.pdf#page=1) · [§2.3, Definition 2.4, p. 63](reiter.pdf#page=7)

## Passages to cite

- **Diagnostic starting point, draft §1.** Cite the formal definition for the claim that diagnosis yields fault hypotheses compatible with observed behavior. In the full-adder example just below it, one single-gate hypothesis and two different two-gate hypotheses explain the same observation. Each is minimal because removing a gate from that hypothesis would spoil consistency. [Definition 2.4 and Example 2.2 continued, p. 63](reiter.pdf#page=7)
- **How candidate sets arise.** A conflict is a set of components that cannot all be healthy given the observations. Each diagnosis must contain at least one component from every conflict. Reiter proves that the inclusion-minimal sets satisfying this condition are precisely the diagnoses. [§4.1, Definitions 4.1 and 4.3, Theorem 4.4, p. 67](reiter.pdf#page=11)
- **What more evidence buys.** Competing diagnoses can predict different values at a probe. A measurement that contradicts a diagnosis rules it out. Reiter’s worked example shows how probing the output of a multiplier distinguishes two predictions. [§5, pp. 82–83, especially Example 5.2 and Proposition 5.5](reiter.pdf#page=26)

**Transition to the motor case.** Reiter asks which components could be faulty. The motor study begins with two faults active in simulation and asks which removal would have kept the winding below its limit. [Reiter, Definition 2.4](reiter.pdf#page=7) · [Motor study, §§3.3–4](../mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=7)
