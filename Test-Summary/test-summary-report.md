# Test Summary Report

## 1. Execution Status

**Execution completed for the current Postman collection on 6-Oct-2026.**

The project contains a broader manual test suite than the current executable collection. The report therefore separates **planned test coverage** from **actually executed and assertion-validated coverage**.

## 2. Execution Metrics

| Metric | Result |
|---|---:|
| Manual test cases defined | 25 |
| Test cases with execution activity | 20 |
| Fully assertion-validated test cases | 16 |
| Executed requests without automated assertions | 2 |
| Manual validation required | 1 |
| Partial automated coverage | 1 |
| Not covered by current collection | 5 |
| Postman requests in collection | 17 |
| Postman assertions | 43 |
| Assertions passed | 43 |
| Assertions failed | 0 |
| Postman execution errors | 0 |
| Confirmed defects | 0 |

## 3. Assertion Result

**43/43 Postman assertions passed.**

The assertions cover endpoint-specific checks such as HTTP status codes, response time, response arrays, product/cart IDs, product creation data, and deletion status.

## 4. Coverage Gaps

The following manual test cases are defined but are **not covered by a corresponding request in the current collection**:

- `TC007` — Invalid product ID
- `TC011` — Create product missing title
- `TC017` — Invalid cart ID
- `TC024` — Empty search parameter
- `TC025` — Unsupported HTTP method

`TC002` and `TC004` have corresponding requests in the collection, but those requests currently contain no automated assertions.

`TC021` requires Content-Type validation, but the collection does not assert the Content-Type header.

`TC022` has partial automated coverage because the collection checks the product ID but does not fully validate all fields listed in the manual test case.

## 5. Defect Status

**No confirmed defects were recorded.**

The project deliberately avoids converting unexecuted or unverified scenarios into defect reports.

## 6. Conclusion

The current Postman collection executed successfully with **43/43 assertions passing and zero execution errors**.

The project demonstrates both:
- practical API execution and automated response assertions in Postman, and
- professional QA discipline by clearly documenting the difference between **planned coverage, executed coverage, and assertion-backed results**.

## 7. Recommended Next Iteration

To increase coverage, add dedicated Postman requests/assertions for the five currently uncovered scenarios and add assertions for invalid authentication, Content-Type, and full response-schema validation.
