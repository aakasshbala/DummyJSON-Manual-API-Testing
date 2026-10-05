# DummyJSON API – Manual API Testing Project

## 1. Project Overview
A portfolio-focused **manual API testing project** using **Postman** against the publicly available DummyJSON REST API.

The project demonstrates practical QA activities including requirements analysis, test-scenario design, test-case design, test-data preparation, Postman request execution, response validation, HTTP status-code validation, negative testing, basic response-time checks, and execution reporting.

> **Execution integrity:** The project separates the full manual test suite from the scenarios actually covered by the current Postman collection. No unexecuted scenario is presented as a passing result.

## 2. Application Under Test
| Item | Details |
|---|---|
| API | DummyJSON |
| Base URL | `https://dummyjson.com` |
| API type | REST / JSON |
| Testing tool | Postman |
| Testing approach | Manual API testing with Postman assertions |
| Execution date | 6-Oct-2026 |

## 3. Testing Scope
- Authentication and bearer-token handling
- Product retrieval and search
- Product creation, update, patch and delete simulation
- Cart retrieval and update simulation
- Query parameters and pagination
- Request-body and response validation
- HTTP status-code validation
- Positive and negative test design
- Basic response-time validation
- Postman assertions and collection execution

## 4. QA Artifacts
- `Requirements/Requirements.md` — functional and quality requirements
- `Test-Scenarios/test-scenarios.xlsx` — planned test scenarios and coverage
- `Test-Cases/test-cases.xlsx` — 25 detailed API test cases
- `Test-Data/test-data.xlsx` — reusable test data
- `Test-Execution/test-execution.xlsx` — execution results and collection coverage
- `Test-Summary/test-summary-report.md` — execution summary
- `Bug-Reports/README.md` — defect-reporting status
- `Postman/DummyJSON-Manual-API-Testing.postman_collection.json` — importable Postman collection

## 5. Postman Execution Results
The current Postman collection contains **17 requests** and the recorded collection run produced:

| Metric | Result |
|---|---:|
| Postman requests | 17 |
| Assertions | 43 |
| Assertions passed | 43 |
| Assertions failed | 0 |
| Execution errors | 0 |
| Confirmed defects | 0 |

The collection includes automated assertions for status codes, response time, selected response fields, arrays, IDs, and other endpoint-specific checks.

## 6. Test Suite Coverage
The project contains **25 manual API test cases**.

- **16** test cases have direct assertion-backed coverage.
- **2** test cases have an executed request but no automated assertion (`TC002`, `TC004`).
- **1** test case requires manual Content-Type validation (`TC021`).
- **1** test case has partial automated response-structure coverage (`TC022`).
- **5** test cases are not covered by the current Postman collection (`TC007`, `TC011`, `TC017`, `TC024`, `TC025`).

This distinction is intentional: a test case is not marked Pass merely because a related request exists.

## 7. Key Execution Notes
The current collection does not contain dedicated requests for:
- Non-existing product ID `99999`
- Missing product title
- Non-existing cart ID `99999`
- Empty product-search query
- Unsupported `HEAD` method

The collection also contains the invalid-login and invalid-token requests, but those two requests currently have **no automated test assertions**. They are therefore recorded as executed without assertion-backed validation rather than being falsely marked as automated Pass.

## 8. Expected API Workflow
Login → capture access token → validate authenticated user → retrieve/search products → create/update/delete product simulation → retrieve/update cart → validate HTTP status behavior.

## 9. Project Note
DummyJSON is a practice API. Its create/update/delete endpoints simulate changes rather than permanently modifying server data. This behavior is considered when defining expected results.

## 10. Reference
DummyJSON documentation: https://dummyjson.com/docs
