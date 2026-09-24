---
name: ui-test-playwright
description: Browser automation testing skill using Playwright for UI testing
---

## Workflow of playwright-ui-test skills
1. Read requirements and use test cases from <user requirement>.
2. Generate test cases for each identified flow using the Playwright framework and use locators with test IDs for reliable element selection.
3. Run the generated test cases and validate the results
4. If the test cases fail, analyze the failure and fix the issues in the application or test cases and run until all test cases pass successfully.


## Project structure
```
tests/
  ├── features/
  │   └── feature.flow.success.spec.ts
  │   └── feature.flow.failure.spec.ts
  ├── pages/
  │   └── login.page.ts
  │   └── dashboard.page.ts
  └── utils/
      └── helper.ts
```

## Playwright UI Test best practices
1. Use selector with test IDs to make tests more reliable and less prone to break due to UI changes.
1. Use descriptive test names and organize tests into logical groups.
2. Use page objects to encapsulate UI interactions and improve test maintainability.
3. Use assertions to validate expected behavior and outcomes.
4. Keep tests independent and avoid relying on the state of other tests.