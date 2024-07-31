# What is an API?

**Definition:**
API (Application Programming Interface) is a set of protocols, routines, and tools that allow different software applications to communicate with each other. APIs define the methods and data structures that developers can use to interact with external software components, operating systems, or microservices.

**Purpose:**
- **Integration:** Enables different systems and applications to work together.
- **Abstraction:** Hides the complex implementation details and provides a simple interface.
- **Reusability:** Promotes code reuse by allowing developers to leverage existing functionality.

**Components of an API:**
1. **Endpoint:** A specific URL where the API can be accessed.
2. **Request:** The data sent to the API, often including headers, parameters, and a body.
3. **Response:** The data returned by the API, usually in JSON or XML format.
4. **Methods:** The actions that can be performed (e.g., GET, POST, PUT, DELETE).

## What is API Testing?

**Definition:**
API testing is a type of software testing that involves testing application programming interfaces (APIs) directly and as part of integration testing to determine if they meet expectations for functionality, reliability, performance, and security.

**Purpose:**
- **Validation:** Ensures the API works as expected and meets the requirements.
- **Reliability:** Tests the API's robustness and error-handling capabilities.
- **Performance:** Evaluates the API's performance under various conditions.
- **Security:** Identifies potential security vulnerabilities.

**Types of API Testing:**
- **Functional Testing:** Verifies that the API performs its intended functions correctly.
- **Load Testing:** Assesses the API's performance under heavy load conditions.
- **Security Testing:** Checks for vulnerabilities and ensures secure data transmission.
- **Integration Testing:** Ensures the API works well with other APIs and components.

## Sample API Testing Scenarios

### Sample 1: User Authentication API

**Endpoint:** `POST /api/v1/auth/login`

**Request:**
```
json
{
  "username": "testuser",
  "password": "testpassword"
}
```

**Response:**
```
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}
```
**Test Cases:**

Valid Credentials:
Request: Valid username and password.
Expected Result: Status code 200, valid token returned.
Invalid Credentials:
Request: Invalid username or password.
Expected Result: Status code 401, error message "Invalid credentials".
Missing Fields:
Request: Missing username or password.
Expected Result: Status code 400, error message "Missing required fields".

### Sample 2: Get User Profile API
Endpoint: `GET /api/v1/users/{user_id}`

**Request Headers:**
```
{
  "Authorization": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}
```
**Response:**
```
{
  "id": "12345",
  "username": "testuser",
  "email": "testuser@example.com",
  "name": "Test User"
}
```
**Test Cases:**

Valid Token:
Request: Valid user ID and authorization token.
Expected Result: Status code 200, user profile data returned.
Invalid Token:
Request: Valid user ID and invalid authorization token.
Expected Result: Status code 401, error message "Unauthorized".
User Not Found:
Request: Invalid user ID and valid authorization token.
Expected Result: Status code 404, error message "User not found".

### Sample 3: Update User Profile API
Endpoint: `PUT /api/v1/users/{user_id}`

**Request Headers:**
```
{
  "Authorization": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}
```
**Request Body:**
```
{
  "email": "newemail@example.com",
  "name": "New Name"
}
```
**Response:**
```
{
  "id": "12345",
  "username": "testuser",
  "email": "newemail@example.com",
  "name": "New Name"
}
```
**Test Cases:**

Valid Update:
Request: Valid user ID, authorization token, and updated profile data.
Expected Result: Status code 200, updated profile data returned.
Invalid Token:
Request: Valid user ID, invalid authorization token, and updated profile data.
Expected Result: Status code 401, error message "Unauthorized".
Invalid Data:
Request: Valid user ID, valid authorization token, and invalid profile data (e.g., invalid email format).
Expected Result: Status code 400, error message "Invalid data".
