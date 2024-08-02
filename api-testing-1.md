# API testing-1

#### 1. **What is an API and why is it important?**

* **Answer:** An API (Application Programming Interface) is a set of rules and protocols for building and interacting with software applications. It allows different software systems to communicate with each other. APIs are important because they enable the integration of different systems and the automation of tasks.

#### 2. **What are the common types of APIs?**

* **Answer:** The common types of APIs include:
  * **REST (Representational State Transfer) APIs**
  * **SOAP (Simple Object Access Protocol) APIs**
  * **GraphQL APIs**
  * **RPC (Remote Procedure Call) APIs**

#### 3. **What is REST API and how does it differ from SOAP API?**

* **Answer:** A REST API (Representational State Transfer) uses HTTP requests to perform CRUD operations (Create, Read, Update, Delete) and is stateless. SOAP (Simple Object Access Protocol) is a protocol that uses XML to exchange information and requires strict standards.
* **Example:**
  * **REST:** `GET /users/123`
  * **SOAP:** A SOAP request involves a more complex XML structure.

#### 4. **How do you test an API?**

* **Answer:** API testing involves the following steps:
  * **Understand the API specifications and endpoints.**
  * **Create test cases for different scenarios (positive, negative, edge cases).**
  * **Use tools like Postman, SoapUI, or curl to send requests and verify responses.**
  * **Validate response status codes, headers, and body.**
  * **Check for performance and security aspects.**

#### 5. **What is the difference between GET and POST methods in HTTP?**

* **Answer:**
  * **GET** retrieves data from a server at the specified resource.
  * **POST** sends data to a server to create or update a resource.
* **Example:**
  * **GET:** `curl http://example.com/api/users/123`
  * **POST:** `curl -X POST -d '{"name":"John"}' http://example.com/api/users`

#### 6. **What are HTTP status codes? Provide examples.**

* **Answer:** HTTP status codes indicate the result of an HTTP request.
  * **200 OK:** The request was successful.
  * **201 Created:** A new resource has been created.
  * **400 Bad Request:** The request was invalid.
  * **401 Unauthorized:** Authentication is required.
  * **404 Not Found:** The requested resource was not found.
  * **500 Internal Server Error:** The server encountered an error.

#### 7. **How do you handle authentication in API testing?**

* **Answer:** Authentication can be handled in various ways, such as:
  * **Basic Authentication:** `curl -u username:password http://example.com/api`
  * **Token-based Authentication:** `curl -H "Authorization: Bearer token" http://example.com/api`
  * **OAuth:** Use tools like Postman to handle OAuth flows and obtain tokens.

#### 8. **What is JSON and how is it used in API testing?**

* **Answer:** JSON (JavaScript Object Notation) is a lightweight data-interchange format. It's easy for humans to read and write, and easy for machines to parse and generate. In API testing, JSON is often used to structure request and response payloads.
*   **Example:**

    ```json
    {
      "id": 123,
      "name": "John",
      "email": "john@example.com"
    }
    ```

#### 9. **What tools do you use for API testing?**

* **Answer:** Common tools for API testing include:
  * **Postman:** For manual and automated API testing.
  * **SoapUI:** For testing SOAP and RESTful web services.
  * **curl:** Command-line tool for sending HTTP requests.
  * **JMeter:** For performance and load testing of APIs.
  * **Newman:** A command-line collection runner for Postman.

#### 10. **Explain how you would test an API for performance.**

* **Answer:**
  * **Identify performance criteria:** Response time, throughput, resource utilization.
  * **Use tools like JMeter or Locust to create and run load tests.**
  * **Simulate multiple users and measure the API's performance under different loads.**
  * **Analyze results to identify bottlenecks and optimize performance.**
