# Responsibility and Blame: A Structural-Model Approach

Hana Chockler and Joseph Y. Halpern (2004). *Journal of Artificial Intelligence Research* 22, 93–115. LaTeX key `chockler2004`. [DOI](https://doi.org/10.1613/jair.1391) · [JAIR PDF hosted at Carnegie Mellon](https://www.cs.cmu.edu/afs/cs/project/jair/pub/volume22/chockler04a.pdf)

## Summary

Chockler and Halpern grade an actual cause by how many other variables must change from their actual values to make it critical to the outcome. If the smallest such number is *k*, the degree of responsibility is **1/(k + 1)**. A cause that already changes the outcome on its own scores 1. An event that fails the causal test scores 0. The authors separately define blame for an action using an agent’s uncertainty before acting. [§3.2, Definition 3.2, p. 99](chockler04a.pdf#page=7) · [§3.3, Definition 3.5, p. 101](chockler04a.pdf#page=9)

## Passages to cite

- **A worked calculation, draft §5.** In a 6–5 election, switching one winning vote reverses the result, so that voter has responsibility 1. In an 11–0 election, five others must switch first for the selected voter to become pivotal. The selected voter’s responsibility is 1/6. [§3.2, Example 3.3, p. 99](chockler04a.pdf#page=7)
- **Why the model matters.** In the bottle-shattering example, adding variables for which rock hits the bottle changes the contingencies available for testing Suzy’s throw. Restricting which settings are allowable can change her score again. [§3.2, Example 3.4, p. 100](chockler04a.pdf#page=8)
- **When to use “blame.”** Definition 3.5 averages the action’s responsibility across situations the agent considers possible, weighted by the agent’s prior probabilities. Use this passage if discussing an agent’s knowledge. [§3.3, pp. 100–101](chockler04a.pdf#page=9)

**Terminology for the motor paper.** Chockler and Halpern’s degree is dimensionless and depends on a count of changes. Mujić and Wotawa’s Eq. (13) takes a difference in a chosen symptom measure. Choosing peak winding temperature gives a difference in degrees Celsius. Cite the motor study for the 17.19 °C drop after friction removal and reserve “degree of responsibility” for the contingency-based quantity. [Definition 3.2, p. 99](chockler04a.pdf#page=7) · [Motor study, Eq. (13)](../mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=7) · [Motor study, Table 2](../mujic-wotawa-2026/OASIcs.DX.2026.16.pdf#page=13)
