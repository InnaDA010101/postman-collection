# Account registration API tests

Postman collection for positive and negative tests of `POST /api/auth/register` on the Playwright Automation practice site.

## Import

In Postman, select **Import** → **Files** and choose `postman-registration-tests.postman_collection.json`. The imported collection appears under **Collections** in the left sidebar.

## Run

Use Collection Runner and run the requests in this order:

1. **Positive - register a new account (201)** generates a unique email and stores it in a collection variable.
2. **Negative - register the same email again (409)** reuses that email to check duplicate handling.
3. **Negative - missing required fields (422)** omits required fields to check validation.

Each request includes Postman tests for the expected status code and JSON response. The base URL and sample values are collection variables and can be edited in Postman.

## Important

The registration endpoint writes to the site's real users table. Run this against the intended test service and use test data. The successful case creates an account each time the collection runs.

