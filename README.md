# 🚀 Booking API Test Automation Framework

## 📌 Project Overview

This project demonstrates end-to-end API test automation for the Restful Booker application:

👉 https://restful-booker.herokuapp.com/apidoc/index.html

It validates core CRUD operations, authentication mechanisms, and negative scenarios using Postman.  
The framework is designed to be CI/CD ready using Newman and Jenkins.

This project showcases:

✔ API functional testing  
✔ Negative & boundary test validation  
✔ Environment variable management  
✔ Automated test execution via CLI  
✔ CI/CD pipeline integration  
✔ HTML test reporting  

---

## 🛠️ Tech Stack

- Postman (API Test Design)
- JavaScript (Postman Test Scripts)
- Newman (CLI Execution)
- Jenkins (CI/CD Integration)
- HTML Reporter
- REST APIs

---

## 📂 Project Structure

Booking API Collection

### 🔹 Positive Endpoints
- Get Booking IDs
- Create Booking
- Get Booking Details
- Token Generator
- Partial Update Booking (PUT)
- Patch Partial Update (PATCH)
- Delete Booking
- Filter Booking with Query Parameter

### 🔹 Negative Endpoints
- Get Booking with Invalid ID
- Get Booking with Blank ID
- Create Booking with Missing Fields
- Create Booking with Invalid Datatype
- Create Booking with Blank Body
- Create Booking with Invalid Date Format
- Create Booking with Extremely Long Input
- Delete Booking without Token
- Filter Booking with Invalid Parameter

---

## 🔐 Authentication Flow

1. Generate token using `/auth`
2. Store token in environment variable
3. Use token for secured operations (PUT / PATCH / DELETE)

---

## 🧪 Test Coverage

### ✔ Functional Testing
- Booking creation and validation
- Data retrieval validation
- Update and delete operations
- Query parameter filtering

### ✔ Negative Testing
- Invalid inputs
- Missing required fields
- Invalid data types
- Unauthorized access
- Invalid path/query parameters

---

# ⚡ Newman Integration (CLI Execution)

Newman allows execution of Postman collections from command line.


### Install Newman
```bash
npm install -g newman
Run Collection
newman run Booking_API_Collection.json \
-e Booking_Environment.json \
-r cli,html \
--reporter-html-export report.html

**Output**
    
    -CLI execution summary
    -HTML execution report
---



---
🔁 Jenkins CI/CD Integration

-  This project supports automated execution using Jenkins.
-  Archive the HTML report as build artifact.


📊 CI Pipeline Benefits
    
   - Automated regression execution
   - Immediate failure detection
   - Execution history tracking
   - Downloadable HTML reports
   - Ready for DevOps workflows

📈 Future Enhancements
    
   - Dockerized execution
   - Parallel execution using Newman
   - Integration with GitHub Actions
   - Slack/email notifications
   - Data-driven execution using CSV/JSON
   - Convert to Rest Assured Framework (Java)
