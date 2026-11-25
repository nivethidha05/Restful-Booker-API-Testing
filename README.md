# Restful Booker API Testing

## Project Overview
This project demonstrates API testing using Postman, JavaScript and Newman. The Restful Booker public practice API is used to validate booking operations, response data, authentication and error handling.

## Tools & Technologies
- Postman
- JavaScript
- REST API
- JSON
- Newman
- CSV (Data-Driven Testing)
- GitHub

## API Operations Tested
- GET – Retrieve booking IDs and booking details
- POST – Create bookings and generate authentication tokens
- PUT – Update existing booking details
- DELETE – Delete bookings

## Testing Activities
- Validated HTTP status codes and response times.
- Verified response body fields and data types.
- Created JavaScript assertions in Postman.
- Used collection variables to store and reuse booking IDs and authentication tokens.
- Implemented request chaining between API requests.
- Validated updated booking details.
- Verified deleted bookings return HTTP 404.
- Implemented CSV-driven testing using Postman Collection Runner and Newman.

## CSV Data-Driven Testing
Created a CSV file containing three booking data sets with different:
- First and last names
- Total prices
- Deposit payment values
- Check-in and check-out dates
- Additional requirements

Used `pm.iterationData.get()` to read test data dynamically and validate API responses.

## Newman Execution Results

| Metric | Result |
|---|---:|
| Iterations | 3 |
| Requests executed | 3 |
| Assertions passed | 27 |
| Assertions failed | 0 |

**Execution Status: PASS**

## Project Files
- `E-Commerce API Testing.postman_collection.json` – Postman API collection.
- `BookingTestData.csv` – CSV test data used for data-driven testing.

## API Reference
[Restful Booker API](https://restful-booker.herokuapp.com/)

## Author
QA Automation Tester | API Testing | Postman | JavaScript | Newman

### Negative API Testing

Designed and executed negative test scenarios to evaluate API input validation and error handling.

**Test scenarios covered:**

| Test Case | Scenario | Actual API Behavior |
|---|---|---|
| TC_009 | Missing First Name | 500 Internal Server Error |
| TC_010 | Missing Last Name | 500 Internal Server Error |
| TC_011 | Invalid Total Price (String) | 200 OK; value converted to null |
| TC_012 | Invalid DepositPaid (String) | 200 OK; value converted to true |
| TC_013 | Invalid Check-in Date Format | 200 OK; invalid date returned |
| TC_014 | Checkout Date Earlier Than Check-in | 200 OK; invalid date range accepted |
| TC_015 | Empty First Name | 200 OK; empty value accepted |
| TC_016 | Empty Last Name | 200 OK; empty value accepted |

**Execution Summary:**
- 8 negative test cases executed.
- 30 JavaScript assertions passed.
- Identified potential API validation weaknesses involving missing fields, invalid data types, empty values and booking dates.
- Used Postman Post-response scripts to validate actual API responses.
