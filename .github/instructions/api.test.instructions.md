---
applyTo: "postman/**/*.json,package.json,README.md,.github/workflows/**/*.yml"
description: "Copilot guidance for Newman/Postman API tests, Allure reports, and CI/CD in this repository."
---

# API Test Guidance

- Keep Newman commands in sync with the Postman collection and environment file paths under `postman/`.
- Use `responseData` for parsed response payloads instead of reusing `json` for multiple meanings.
- Treat `pm.iterationData.get(key)` as optional and fall back to environment values when a test can run without iteration data.
- Keep generated artifacts out of version control: `newman/`, `allure-results/`, `allure-report/`, and `reports/`.
- When adding or changing a test flow, update the README and CI workflow together.
- Prefer the existing scripts in `package.json`: `test:api`, `test:api:devices`, `test:api:allure`, `test:api:devices:allure`, `allure:open`, and `allure:open:devices`.
