# Backend Coding Challenge: KYC (Know Your Customer) Compliance

## Objective
Develop a backend service that handles KYC verifications for customer accounts. The service should integrate with external verification services and ensure that KYC compliance requirements are met.

## Challenge Description

Create a RESTful API that performs the following functions:

### Customer Registration
- **Endpoint:** `POST /customers`
- **Input:** JSON payload with customer details including `customer_id`, `name`, `email`, `phone_number`, `date_of_birth`, `address`, and `identity_document` (e.g., passport or driver's license).
- **Function:** Validate the input data and store the customer details in a database.

### KYC Verification
Implement a KYC verification process that integrates with external KYC services (e.g., identity verification APIs). The service should:
- Send customer identity documents to an external KYC provider for validation.
- Store the verification result and any associated metadata (e.g., verification status, timestamp) in the database.

### Verification Status
- **Endpoint:** `GET /customers/{customer_id}/kyc-status`
- **Input:** Customer ID.
- **Output:** KYC verification status (e.g., "pending", "verified", "rejected") and details of any issues or discrepancies.

### Update Customer Information
- **Endpoint:** `PUT /customers/{customer_id}`
- **Input:** JSON payload with updated customer details.
- **Function:** Update the customer information in the database and trigger a re-verification if necessary.

### Compliance Reporting
- **Endpoint:** `GET /report`
- **Input:** Date range (start and end).
- **Output:** Summary report of KYC verification statuses, including the number of verified, pending, and rejected customers.

## Requirements

1. Implement the API using a modern backend framework (e.g., Express.js for Node.js, Flask for Python, or Spring Boot for Java).
2. Use a relational or NoSQL database to store customer information and verification results.
3. Ensure secure storage and handling of sensitive customer data, including encryption.
4. Write unit tests to validate the functionality of each component.
5. Document the API endpoints and provide clear instructions on how to set up and run the service.

## Bonus Points

- Implement rate limiting to prevent abuse of the KYC verification process.
- Add logging and monitoring to track API usage and detect anomalies.
- Use asynchronous processing (e.g., message queues) to handle verification requests and responses efficiently.
- Provide a mechanism for manual review and intervention if automatic KYC verification fails.

## Submission

- Provide a GitHub repository with your code, including a `README.md` file with instructions on how to set up and run the service.
- Include a brief explanation of your design decisions and any trade-offs you considered.
# kyc
