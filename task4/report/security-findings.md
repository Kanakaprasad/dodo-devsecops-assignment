# Dodo Payments - Task 4B Security Assessment

## Target
Bundled ledger-api application

---

## Finding 1: Sensitive Data Exposure

Severity: High

Endpoint:
GET /transactions

Description:
The endpoint returns complete payment card numbers (PAN), transaction IDs, amount, currency, and status without authentication.

Evidence:

GET /transactions

Response contains:

- Full PAN
- Transaction ID
- Amount
- Currency
- Status

Impact:

- Disclosure of sensitive payment information
- PCI DSS compliance risk
- Information disclosure

Remediation:

- Require authentication and authorization
- Mask PAN values
- Return only the last four digits
- Follow PCI DSS guidance

---

## Finding 2: Server-Side Request Forgery (SSRF)

Severity: High

Endpoint:
GET /fetch?url=

Description:
The endpoint accepts arbitrary user-supplied URLs and performs server-side HTTP requests.

Evidence:

Successfully fetched:

https://example.com

Attempting:

http://127.0.0.1:8080/health

resulted in a timeout. Docker logs confirm the application attempted the request.

Impact:

May allow access to internal services or cloud metadata if reachable.

Remediation:

- Validate URLs
- Use an allow-list
- Block localhost/private IP ranges
- Restrict outbound network access

---

## Finding 3: Unsafe YAML Deserialization

Severity: Medium

Endpoint:
POST /import

Description:

The application uses:

yaml.load(request.data)

on user-controlled input.

Evidence:

A crafted YAML payload reached the YAML constructor and generated a ConstructorError.

Remote code execution was NOT demonstrated during testing.

Remediation:

Replace:

yaml.load(...)

with:

yaml.safe_load(...)

Validate the input schema before processing.
