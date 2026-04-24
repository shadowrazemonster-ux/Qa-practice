# API-ТЕСТИРОВАНИЕ
📌 Project Overview
This repository contains a comprehensive Postman Collection designed to test the REST API of the Automation Exercise platform. The project demonstrates advanced API testing techniques, including functional validation, security constraints, and end-to-end (E2E) user flow testing.

🚀 Key Features
Full CRUD Coverage: Automated tests for Creating, Reading, Updating, and Deleting user accounts.

Negative Testing: Validating API resilience against unauthorized methods (405) and bad requests (400).

Data Validation: Deep JSON schema validation using the Chai.js assertion library.

Dynamic Logic: Conditional testing scripts to handle fluctuating data states.

🛠 Test Suite Details
1. Product & Brand Management
GET All Products List: Validates the retrieval of the full product catalog and ensures the response is a non-empty array.

POST All Products (Negative): Verifies that the endpoint correctly rejects unauthorized POST requests with a 405 status.

GET All Brands List: Ensures the brand directory is accessible and correctly structured.

PUT All Brands (Negative): Validates system behavior when an unsupported PUT method is applied to the brand list.

2. Search Functionality
POST Search Product: Confirms that the search engine returns relevant products based on the search_product parameter.

POST Search Product (Missing Param): Negative test to ensure the API returns a 400 error when required search parameters are absent.

3. Authentication & Security
POST Verify Login (Positive): Validates successful user authentication with valid credentials.

POST Verify Login (Missing Email): Ensures the system blocks login attempts missing essential data.

POST Verify Login (Invalid User): Confirms a 404 response when attempting to log in with non-existent account details.

Method Constraint Check: A security test to ensure the login endpoint rejects DELETE and GET requests where only POST is permitted.

4. Account Lifecycle (End-to-End)
POST Create Account: Automates the registration process using multipart/form-data. Checks for a 201 Created response.

PUT Update Account: Tests the ability to modify existing user profile data (Address, Company, Birthdate).

DELETE Account: Validates the secure removal of user data from the system.

GET User Detail by Email: A final verification step to confirm account status and data integrity post-registration/deletion.

💻 Tech Stack
Tool: Postman Desktop

Scripting: JavaScript (Postman Sandbox)

Library: Chai.js (Assertions)

API Type: REST

📖 How to Run
Clone this repository.

Import the .json collection file into your Postman workspace.

(Optional) Run the entire collection using the Postman Runner or Newman to see all 14 tests pass.

👤 Author
Niyazbek QA Automation / Software Engineering Student at School 21
