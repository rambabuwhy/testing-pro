# curl get requests

#### 1. **Basic GET Request**

* **Question:** How do you perform a basic GET request using `curl`?
* **Answer:** `curl http://example.com`

#### 2. **Custom Headers**

* **Question:** How do you add custom headers to a GET request using `curl`?
* **Answer:** `curl -H "Authorization: Bearer token" http://example.com`

#### 3. **Query Parameters**

* **Question:** How do you include query parameters in a GET request with `curl`?
* **Answer:** `curl "http://example.com?param1=value1&param2=value2"`

#### 4. **Handling Redirects**

* **Question:** How do you follow redirects with `curl`?
* **Answer:** `curl -L http://example.com`

#### 5. **Verbose Output**

* **Question:** How do you enable verbose output to debug a `curl` request?
* **Answer:** `curl -v http://example.com`

#### 6. **Saving Response to a File**

* **Question:** How do you save the response of a GET request to a file using `curl`?
* **Answer:** `curl http://example.com -o output.txt`

#### 7. **Timeouts**

* **Question:** How do you set a timeout for a `curl` GET request?
* **Answer:** `curl --max-time 10 http://example.com`

#### 8. **User Agent**

* **Question:** How do you specify a user agent in a `curl` request?
* **Answer:** `curl -A "Mozilla/5.0" http://example.com`

#### 9. **Handling HTTP Status Codes**

* **Question:** How do you handle different HTTP status codes in a `curl` GET request?
* **Answer:** By checking the HTTP response code using `curl -I http://example.com`

#### 10. **Basic Authentication**

```markdown
Question: How do you perform a GET request with basic authentication using `curl`?
Answer: `curl -u username:password http://example.com`
```

#### 11. **Proxy Usage**

```markdown
Question: How do you make a GET request through a proxy with `curl`?
Answer: `curl -x http://proxyserver:port http://example.com`
```

#### 12. **SSL/TLS Verification**

```markdown
Question: How do you ignore SSL certificate verification in a `curl` request?
Answer: `curl -k https://example.com`
```

#### 13. **Data Parsing**

```markdown
Question: How do you parse the JSON response from a `curl` request in a script?
Answer: By piping the response to a tool like `jq`: `curl http://example.com | jq .`
```

#### 14. **Rate Limiting**

```markdown
Question: How do you handle rate limiting when making multiple `curl` requests?
Answer: Implement a delay between requests using a loop and sleep command in a script.
```

#### 15. **Error Handling**

```markdown
Question: How do you handle errors and retries in `curl`?
Answer: Use `--retry` and `--retry-connrefused`: `curl --retry 3 --retry-connrefused http://example.com`
```

#### 16. **HTTP Methods**

```markdown
markdownCopy code- **Question:** How can you specify different HTTP methods (e.g., GET, POST) in `curl`?
- **Answer:** For GET: `curl http://example.com`, for POST: `curl -X POST http://example.com`
```

#### 17. **Multiple URLs**

```markdown
Question: How do you make `curl` requests to multiple URLs?
Answer: `curl http://example1.com http://example2.com`
```

#### 18. **Debugging Connection Issues**

```markdown
Question: How do you debug connection issues with `curl`?
Answer: Use `curl -v` or `curl -trace-ascii debug.txt http://example.com`
```

#### 19. **Compressed Responses**

```markdown
Question: How do you handle compressed responses in `curl`?
Answer: `curl --compressed http://example.com`
```

#### 20. **Connection Details**

```csharp
Question: How do you get detailed connection information with `curl`?
Answer: `curl -w "@curl-format.txt" -o /dev/null -s http://example.com`
```
