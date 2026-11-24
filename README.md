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
