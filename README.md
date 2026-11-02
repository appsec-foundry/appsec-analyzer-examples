# appsec-analyzer examples

Example security assessments produced by [appsec-analyzer](https://github.com/appsec-foundry/appsec-analyzer). Each assessment includes a report, structured YAML data, and architecture diagrams.

## OWASP Juice Shop

[OWASP Juice Shop](https://github.com/juice-shop/juice-shop) is a deliberately vulnerable web application for security training.

| Assessment depth | Runtime | Estimated cost (USD) | Findings | Report | Data | Diagrams |
|---|---|---|---|---|---|---|
| quick | 22 min | 8 | 51 | [Markdown](juice-shop/security-assessment-juice-shop-quick-v0.1.0.md) | [YAML](juice-shop/security-assessment-juice-shop-quick-v0.1.0.yaml) | [1](juice-shop/security-assessment-juice-shop-quick-v0.1.0.figure1.svg), [1b](juice-shop/security-assessment-juice-shop-quick-v0.1.0.figure1b.svg), [2](juice-shop/security-assessment-juice-shop-quick-v0.1.0.figure2.svg) |
| standard | 40 min | 15 | 104 | [Markdown](juice-shop/security-assessment-juice-shop-standard-v0.1.0.md) | [YAML](juice-shop/security-assessment-juice-shop-standard-v0.1.0.yaml) | [1](juice-shop/security-assessment-juice-shop-standard-v0.1.0.figure1.svg), [1b](juice-shop/security-assessment-juice-shop-standard-v0.1.0.figure1b.svg), [2](juice-shop/security-assessment-juice-shop-standard-v0.1.0.figure2.svg) |
| thorough | 1 h 13 min | 36.36 | 162 | [Markdown](juice-shop/security-assessment-juice-shop-thorough-v0.1.0.md) | [YAML](juice-shop/security-assessment-juice-shop-thorough-v0.1.0.yaml) | [1](juice-shop/security-assessment-juice-shop-thorough-v0.1.0.figure1.svg), [1b](juice-shop/security-assessment-juice-shop-thorough-v0.1.0.figure1b.svg), [2](juice-shop/security-assessment-juice-shop-thorough-v0.1.0.figure2.svg) |

Quick and standard were generated on October 26, 2026; thorough on November 2, 2026. All three reference commit `33518f5`; the thorough report also records local changes.

Model configurations differ between runs and affect runtime, cost, and findings. Each report's **Run Statistics** appendix lists its command, models, and timing.

## DVWA

[DVWA](https://github.com/digininja/DVWA) (Damn Vulnerable Web Application) is a deliberately vulnerable PHP/MariaDB application for security training.

| Assessment depth | Runtime | Estimated cost (USD) | Findings | Report | Data | Diagrams |
|---|---|---|---|---|---|---|
| thorough | 36 min | Not recorded | 73 | [Markdown](dvwa/security-assessment-dvwa-thorough-0.1.0.md) | [YAML](dvwa/security-assessment-dvwa-thorough-0.1.0.yaml) | [1](dvwa/security-assessment-dvwa-thorough-0.1.0.figure1.svg), [1b](dvwa/security-assessment-dvwa-thorough-0.1.0.figure1b.svg), [2](dvwa/security-assessment-dvwa-thorough-0.1.0.figure2.svg) |

Generated on October 30, 2026 from commit `d45ba3c`.

## Reading the examples

- **Markdown** contains the assessment: architecture, findings, evidence, and proposed mitigations.
- **YAML** contains the structured assessment data.
- **Diagrams** show runtime architecture (1), supply chain and build (1b), and attack routes and impact (2). Each SVG also has a `-dark.svg` variant.

Finding counts refer to the entries in each report's findings register. Summaries may group findings by weakness and show different totals.

Runtimes are rounded from the reports' wall-clock statistics. Costs are estimates at API list prices; subscription billing differs. The reports are based on automated static analysis of code and configuration.
