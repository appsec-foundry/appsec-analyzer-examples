# appsec-analyzer examples

Example reports produced by [appsec-analyzer](https://github.com/appsec-foundry/appsec-analyzer). They show what the tool outputs at each assessment depth, so you can compare the modes without running it yourself.

## OWASP Juice Shop

[OWASP Juice Shop](https://github.com/juice-shop/juice-shop) is a deliberately insecure web application used for security training and tool testing.

### Latest thorough example

The `v0.6.0b6` artifact set was generated on November 2, 2026 from commit `33518f5` with local changes, as recorded in the report's run statistics.

| Depth | Runtime | Cost (approx.) | Findings | Report | Data | Diagrams |
|---|---|---|---|---|---|---|
| thorough | 1 h 13 min 15 s | USD 36.36 | 162 | [md](juice-shop/security-assessment-juice-shop-thorough-v0.6.0b6.md) | [yaml](juice-shop/security-assessment-juice-shop-thorough-v0.6.0b6.yaml) | [1](juice-shop/security-assessment-juice-shop-thorough-v0.6.0b6.figure1.svg), [1b](juice-shop/security-assessment-juice-shop-thorough-v0.6.0b6.figure1b.svg), [2](juice-shop/security-assessment-juice-shop-thorough-v0.6.0b6.figure2.svg) |

- Run with `--hard-budget 40 --assessment-depth thorough --trust-mode untrusted`, using Opus 5.5 for survey, verification, and threat merging, Sonnet 5.5 for supporting stages, and Haiku 5.5 for reconnaissance.
- The count above is the findings register total; the report also groups findings into 42 weakness classes.
- Cost is an estimate at API list prices; subscription billing differs.
- Every diagram also exists as a `-dark` variant (`…figure1-dark.svg`).

### Assessment depth comparison (`v0.1.0`)

These three assessments analyze commit `33518f5` at different assessment depths (`--assessment-depth`).

| Depth | Runtime | Cost (approx.) | Threats | Report | Data | Diagrams |
|---|---|---|---|---|---|---|
| quick | 22 min | USD 8 | 51 | [md](juice-shop/security-assessment-juice-shop-quick-v0.1.0.md) | [yaml](juice-shop/security-assessment-juice-shop-quick-v0.1.0.yaml) | [1](juice-shop/security-assessment-juice-shop-quick-v0.1.0.figure1.svg), [1b](juice-shop/security-assessment-juice-shop-quick-v0.1.0.figure1b.svg), [2](juice-shop/security-assessment-juice-shop-quick-v0.1.0.figure2.svg) |
| standard | 41 min | USD 15 | 104 | [md](juice-shop/security-assessment-juice-shop-standard-v0.1.0.md) | [yaml](juice-shop/security-assessment-juice-shop-standard-v0.1.0.yaml) | [1](juice-shop/security-assessment-juice-shop-standard-v0.1.0.figure1.svg), [1b](juice-shop/security-assessment-juice-shop-standard-v0.1.0.figure1b.svg), [2](juice-shop/security-assessment-juice-shop-standard-v0.1.0.figure2.svg) |
| thorough | 1 h 36 min | USD 40 | 147 | [md](juice-shop/security-assessment-juice-shop-thorough-v0.1.0.md) | [yaml](juice-shop/security-assessment-juice-shop-thorough-v0.1.0.yaml) | [1](juice-shop/security-assessment-juice-shop-thorough-v0.1.0.figure1.svg), [1b](juice-shop/security-assessment-juice-shop-thorough-v0.1.0.figure1b.svg), [2](juice-shop/security-assessment-juice-shop-thorough-v0.1.0.figure2.svg) |

- Quick and standard ran on Sonnet 5.5, thorough on Sonnet 5.5 plus Opus 5.5 for selected steps.
- The thorough run reused model calls from an earlier run (about USD 37 of its total); its final run took 22 min, while the 1 h 36 min total includes the earlier run.
- Every diagram also exists as a `-dark` variant (`…figure1-dark.svg`).

## DVWA

[DVWA](https://github.com/digininja/DVWA) (Damn Vulnerable Web Application) is a deliberately vulnerable PHP/MariaDB application for security training. One thorough assessment, analyzed at commit `d45ba3c`.

| Depth | Runtime | Cost (approx.) | Threats | Report | Data | Diagrams |
|---|---|---|---|---|---|---|
| thorough | 33 min | n/a | 73 | [md](dvwa/security-assessment-dvwa-thorough-0.1.0.md) | [yaml](dvwa/security-assessment-dvwa-thorough-0.1.0.yaml) | [1](dvwa/security-assessment-dvwa-thorough-0.1.0.figure1.svg), [1b](dvwa/security-assessment-dvwa-thorough-0.1.0.figure1b.svg), [2](dvwa/security-assessment-dvwa-thorough-0.1.0.figure2.svg) |

- Run with `--hard-budget 30.0 --assessment-depth thorough --trust-mode untrusted`, using Opus 5.5 for the reasoning steps.
- Every diagram also exists as a `-dark` variant.
