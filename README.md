# appsec-analyzer examples

Example reports produced by [appsec-analyzer](https://github.com/appsec-foundry/appsec-analyzer). They show what the tool outputs at each assessment depth, so you can compare the modes without running it yourself.

## OWASP Juice Shop

[OWASP Juice Shop](https://github.com/juice-shop/juice-shop) is a deliberately insecure web application used for security training and tool testing. All three assessments analyze it at commit `33518f5` and differ only in the assessment depth (`--assessment-depth`).

| Depth | Runtime | Cost (approx.) | Threats | Report | Data | Diagrams |
|---|---|---|---|---|---|---|
| quick | 22 min | USD 8 | 51 | [md](security-assessment-juice-shop-quick-v0.1.0.md) | [yaml](security-assessment-juice-shop-quick-v0.1.0.yaml) | [1](security-assessment-juice-shop-quick-v0.1.0.figure1.svg), [1b](security-assessment-juice-shop-quick-v0.1.0.figure1b.svg), [2](security-assessment-juice-shop-quick-v0.1.0.figure2.svg) |
| standard | 41 min | USD 15 | 104 | [md](security-assessment-juice-shop-standard-v0.1.0.md) | [yaml](security-assessment-juice-shop-standard-v0.1.0.yaml) | [1](security-assessment-juice-shop-standard-v0.1.0.figure1.svg), [1b](security-assessment-juice-shop-standard-v0.1.0.figure1b.svg), [2](security-assessment-juice-shop-standard-v0.1.0.figure2.svg) |
| thorough | 1 h 36 min | USD 40 | 147 | [md](security-assessment-juice-shop-thorough-v0.1.0.md) | [yaml](security-assessment-juice-shop-thorough-v0.1.0.yaml) | [1](security-assessment-juice-shop-thorough-v0.1.0.figure1.svg), [1b](security-assessment-juice-shop-thorough-v0.1.0.figure1b.svg), [2](security-assessment-juice-shop-thorough-v0.1.0.figure2.svg) |

- Quick and standard ran on Sonnet 5.5, thorough on Sonnet 5.5 plus Opus 5.5 for selected steps.
- The thorough run reused model calls from an earlier run (about USD 37 of its total); the 22 min were the final run, 1 h 36 min include the earlier one.
- Every diagram also exists as a `-dark` variant (`…figure1-dark.svg`).
