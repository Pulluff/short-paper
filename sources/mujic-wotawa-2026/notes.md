# Counterfactual Fault Responsibility in a Dynamic Structural Causal Model of a DC Motor

Emir Mujić and Franz Wotawa (2026). *37th International Conference on Principles of Diagnosis and Resilient Systems (DX 2026)*, OASIcs 148, article 16, pp. 16:1–16:14. LaTeX key `mujic2026`. [DOI](https://doi.org/10.4230/OASIcs.DX.2026.16) · [Publisher PDF](https://drops.dagstuhl.de/storage/01oasics/oasics-vol148-dx2026/OASIcs.DX.2026.16/OASIcs.DX.2026.16.pdf)

## Summary

Which fault explains a hot winding when a motor still follows its commanded motion? Mujić and Wotawa simulate the same task with individual faults switched off. In their second experiment, partial demagnetization (FEF4) and excess viscous friction (FMF1) both raise the peak winding temperature. Removing friction lowers the current needed to follow the task and keeps the winding below 90 °C. Removing demagnetization still leaves the winding above that limit. [§5.2 and Fig. 3, pp. 16:11–16:12](OASIcs.DX.2026.16.pdf#page=11)

## Evidence for the case analysis

The peaks and 90 °C outcomes below come from the authors’ simulations. The drop column subtracts each reported peak from the factual peak. [Table 2, p. 16:13](OASIcs.DX.2026.16.pdf#page=13)

| Fault removed | Peak winding temperature | Drop from factual peak | Reached 90 °C? |
|---|---:|---:|:---:|
| None (both active) | 105.70 °C | — | Yes |
| Partial demagnetization (FEF4) | 96.52 °C | 9.18 °C | Yes |
| Excess viscous friction (FMF1) | 88.51 °C | 17.19 °C | No |
| Both | 81.30 °C | 24.40 °C | No |

## Passages to cite

- **Method, draft §3.** Each branch starts from the same state and follows the same reference and load profile. The controller recomputes its voltage command as the motor responds. Equation (12) keeps the other faults at their factual settings. Equation (13) defines responsibility as the factual symptom score minus the score after removal. [§3.3, Eqs. (11)–(13), p. 16:7](OASIcs.DX.2026.16.pdf#page=7)
- **Severity and necessity, draft §4.** The authors count a peak reduction greater than 5 °C as a severity contribution. Equation (18) defines the event as reaching or exceeding 90 °C. Equation (19) tests whether removing a fault prevents that event. The thermal cost combines squared winding and housing temperature excesses across time and is a separate column in Table 2. [Eq. (15), p. 16:9](OASIcs.DX.2026.16.pdf#page=9) · [§4.2, Eqs. (18)–(19), p. 16:10](OASIcs.DX.2026.16.pdf#page=10)
- **Robustness and scope, draft §5.** The friction attribution held in 84 of 100 repetitions with varied model parameters. The study assumes known fault mechanisms, generates and evaluates trajectories in the same model class, and initializes each branch from the true simulated state. A real motor would require state estimates from noisy measurements. [Test design, p. 16:8](OASIcs.DX.2026.16.pdf#page=8) · [Result, p. 16:12](OASIcs.DX.2026.16.pdf#page=12) · [§6, p. 16:13](OASIcs.DX.2026.16.pdf#page=13)

## Deduction for the short paper

If the draft defines overheating at **100 °C**, the factual peak still qualifies and both single-removal peaks fall below it. Either removal would therefore prevent this newly defined event in the published trajectories. Present this as the draft’s threshold thought experiment and cite Table 2 for its inputs. [Table 2, p. 16:13](OASIcs.DX.2026.16.pdf#page=13)
