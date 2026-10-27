# appsec-analyzer examples

Example reports produced by [appsec-analyzer](https://github.com/appsec-foundry/appsec-analyzer). They show what the tool outputs at each assessment depth, so you can compare the modes without running it yourself.

## Juice Shop

All three reports analyze [OWASP Juice Shop](https://github.com/juice-shop/juice-shop) at commit `33518f5` and differ only in the assessment depth (`--assessment-depth`).

| Depth | Model | Threats | Generated | Report | Data |
|---|---|---|---|---|---|
| quick | Sonnet 5.5 | 51 | 2026-10-26 | [md](security-assessment-juice-shop-quick-v0.1.0.md) | [yaml](security-assessment-juice-shop-quick-v0.1.0.yaml) |
| standard | Sonnet 5.5 | 104 | 2026-10-26 | [md](security-assessment-juice-shop-standard-v0.1.0.md) | [yaml](security-assessment-juice-shop-standard-v0.1.0.yaml) |
| thorough | Opus 5.5 | 147 | 2026-10-27 | [md](security-assessment-juice-shop-thorough-v0.1.0.md) | [yaml](security-assessment-juice-shop-thorough-v0.1.0.yaml) |

## Files

Each run produces:

- `security-assessment-<project>-<depth>-v<version>.md`: the readable report
- `security-assessment-<project>-<depth>-v<version>.yaml`: the same results as structured data
- `security-assessment-<project>-<depth>-v<version>.figure*.svg`: diagrams embedded in the report, each with a `-dark` variant

More example projects may be added later.
