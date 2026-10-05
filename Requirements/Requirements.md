# API Testing Requirements

## 1\. Purpose

These requirements define the functional and quality expectations used to design the manual API test suite for the DummyJSON practice API.

## 2\. Functional Requirements

|ID|Requirement|
|-|-|
|REQ-001|API should allow a valid user to authenticate using valid credentials.|
|REQ-002|API should return an access token after successful authentication.|
|REQ-003|Authenticated user details should be retrievable using a valid bearer token.|
|REQ-004|Protected user endpoints should reject invalid authentication where authentication is required.|
|REQ-005|API should return product collection data through the products endpoint.|
|REQ-006|API should support retrieving a product by ID.|
|REQ-007|API should support product search using a query parameter.|
|REQ-008|API should support product pagination using `limit` and `skip`.|
|REQ-009|API should support simulated product creation through POST.|
|REQ-010|API should support simulated product update through PUT.|
|REQ-011|API should support simulated partial product update through PATCH.|
|REQ-012|API should support simulated product deletion through DELETE.|
|REQ-013|API should return cart information for valid cart IDs.|
|REQ-014|API should support simulated cart update through PUT.|
|REQ-015|API should return appropriate HTTP status codes for valid and invalid requests.|
|REQ-016|API responses should contain valid JSON where applicable.|

## 3\. Quality Requirements

|ID|Requirement|
|-|-|
|NFR-001|Response time should remain below the project threshold of 3000 ms for checks where the threshold is applied.|
|NFR-002|JSON API responses should return an appropriate Content-Type.|
|NFR-003|Response bodies should follow the documented structure for the endpoint under test.|

## 4\. Coverage Note

These requirements support the **25-case manual test suite**. The current Postman collection provides executable coverage for 17 requests; therefore, not every requirement/scenario is represented by an automated assertion in the current collection.

Uncovered scenarios are retained in the test suite so that the portfolio demonstrates test-design thinking without presenting unexecuted scenarios as executed results.

