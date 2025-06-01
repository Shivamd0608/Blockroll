# BlockRoll - The Ultimate Payment App

## API Documentation

### Endpoint: `/users/register`

#### Description:
This endpoint is used to register a new user in the BlockRoll system. The user can register as an employer, freelancer, or a normal user.

#### HTTP Method:
`POST`

#### Request Body:
The endpoint expects the following data in JSON format:

```json
{
  "username": "string",       // Required. The username of the user.
  "user_type": "string"       // Required. The type of user. Possible values: "employer", "freelancer", "normal".
}
```

#### Response:

##### Success Response:
- **Status Code:** `201 Created`
- **Body:**
  ```json
  {
    "message": "User registered successfully",
    "data": {
      "username": "string",
      "user_type": "string",
      "account": "string" // Blockchain account address of the user
    }
  }
  ```

##### Error Responses:
1. **Missing Fields**
   - **Status Code:** `400 Bad Request`
   - **Body:**
     ```json
     {
       "error": "Username and user_type are required"
     }
     ```

2. **User Already Registered**
   - **Status Code:** `409 Conflict`
   - **Body:**
     ```json
     {
       "error": "User is already registered"
     }
     ```

3. **Internal Server Error**
   - **Status Code:** `500 Internal Server Error`
   - **Body:**
     ```json
     {
       "error": "An error occurred while registering the user"
     }
     ```

#### Example Request:
```bash
curl -X POST http://localhost:5000/users/register \
-H "Content-Type: application/json" \
-d '{
  "username": "shivam",
  "user_type": "freelancer"
}'
```

---

## Updates
- Renamed all occurrences of "shivam oha" to "shivam dubey" across the project files.
```// filepath: c:\Users\shivam dubey\Desktop\ojha sir proj\Blockroll\README.md
# BlockRoll - The Ultimate Payment App

## API Documentation

### Endpoint: `/users/register`

#### Description:
This endpoint is used to register a new user in the BlockRoll system. The user can register as an employer, freelancer, or a normal user.

#### HTTP Method:
`POST`

#### Request Body:
The endpoint expects the following data in JSON format:

```json
{
  "username": "string",       // Required. The username of the user.
  "user_type": "string"       // Required. The type of user. Possible values: "employer", "freelancer", "normal".
}
```

#### Response:

##### Success Response:
- **Status Code:** `201 Created`
- **Body:**
  ```json
  {
    "message": "User registered successfully",
    "data": {
      "username": "string",
      "user_type": "string",
      "account": "string" // Blockchain account address of the user
    }
  }
  ```

##### Error Responses:
1. **Missing Fields**
   - **Status Code:** `400 Bad Request`
   - **Body:**
     ```json
     {
       "error": "Username and user_type are required"
     }
     ```

2. **User Already Registered**
   - **Status Code:** `409 Conflict`
   - **Body:**
     ```json
     {
       "error": "User is already registered"
     }
     ```

3. **Internal Server Error**
   - **Status Code:** `500 Internal Server Error`
   - **Body:**
     ```json
     {
       "error": "An error occurred while registering the user"
     }
     ```

#### Example Request:
```bash
curl -X POST http://localhost:5000/users/register \
-H "Content-Type: application/json" \
-d '{
  "username": "shivam",
  "user_type": "freelancer"
}'
```

---

## Updates
- Renamed all occurrences of "shivam oha" to "shivam dubey" across the project files.