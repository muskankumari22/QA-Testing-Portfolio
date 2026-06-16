# Login API Test Cases

## API Details
- Method: POST
- Endpoint: /api/login

## Test Cases

### TC_API_001 - Valid Login

**Request:**
```json
{
  "email": "user@test.com",
  "password": "Password123"
}
```

**Expected Result:**
- Status Code: 200 OK
- Login successful
- Authentication token returned

---

### TC_API_002 - Invalid Password

**Request:**
```json
{
  "email": "user@test.com",
  "password": "WrongPassword"
}
```

**Expected Result:**
- Status Code: 401 Unauthorized
- Error message returned

---

### TC_API_003 - Empty Email

**Request:**
```json
{
  "email": "",
  "password": "Password123"
}
```

**Expected Result:**
- Status Code: 400 Bad Request
- Validation error for email field

---

### TC_API_004 - Empty Password

**Request:**
```json
{
  "email": "user@test.com",
  "password": ""
}
```

**Expected Result:**
- Status Code: 400 Bad Request
- Validation error for password field
