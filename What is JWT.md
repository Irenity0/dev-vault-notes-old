### **What is JWT (JSON Web Token)?**

**JSON Web Token (JWT)** is a secure way to transfer information between two parties (e.g., client and server) as a digitally signed token. It is commonly used for **authentication** and **authorization** in web applications.

---

### **Structure of a JWT**

A JWT is a string divided into three parts, separated by dots (`.`):

```css
Header.Payload.Signature
```

1. **Header**:  
Contains metadata about the token, including the algorithm used for signing (e.g., `HS256`) and the token type.  
Example:

```json
{
  "alg": "HS256",
  "typ": "JWT"
}
```

2. **Payload**:  
Contains the actual data (claims) about the user or session. This is often encoded but not encrypted, meaning it’s readable if decoded.  
Example:

```json
{
  "userId": "12345",
  "role": "admin",
  "exp": 1675275600
}
```

3. **Signature**:  
Ensures the token’s integrity and authenticity by signing the Header and Payload using a secret key or private key.

### **How JWT Works**

1. **User Login**:
    
    - A user logs in with their credentials (e.g., username and password).
    - The server verifies the credentials and generates a JWT containing user information (e.g., `userId`, `role`).
    - The JWT is signed using a secret key and sent back to the client.
2. **Token Storage**:
    
    - The client stores the JWT (commonly in **localStorage** or **cookies**).
3. **Making Requests**:
    
    - The client includes the JWT in the **Authorization header** (e.g., `Bearer <token>`) of API requests.
4. **Token Validation**:
    
    - The server validates the token’s signature and checks claims like expiration (`exp`).
    - If valid, the server processes the request; otherwise, it rejects it.

---

### **Key Features of JWT**

1. **Self-contained**:
    
    - JWT includes all necessary information (e.g., user data, expiration) to verify itself. No need to query the database on every request.
2. **Stateless**:
    
    - The server doesn’t need to store session information, making JWT ideal for scalable systems.
3. **Secure**:
    
    - The token is signed, ensuring data integrity. However, the payload is not encrypted unless additional encryption is applied.
4. **Compact**:
    
    - Its small size makes it ideal for use in HTTP headers or URLs.

---

### **Common Use Cases**

1. **Authentication**:  
    Verifying a user’s identity after login.
2. **Authorization**:  
    Granting or denying access based on the user’s role or claims.
3. **Information Exchange**:  
    Securely transmitting information between two parties.

---

### **Advantages**

- **Efficient**: Lightweight and reduces the need for server-side session storage.
- **Cross-platform**: Can be used in multiple programming languages.
- **Stateless**: The server doesn't need to maintain session state.

### **Disadvantages**

- **Payload Visibility**: The data in the payload is base64 encoded but not encrypted, so sensitive information should not be included.
- **Token Revocation**: JWTs can’t be easily revoked unless a blacklist system is implemented.

---

### **Example JWT Token**

```plaintext
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9
.eyJ1c2VySWQiOiIxMjM0NSIsInJvbGUiOiJhZG1pbiIsImV4cCI6MTY3NTI3NTYwMH0
.mI4P3drROKwSxH7bEhCd2J9o7ZXLWW2dNyM6lZZgYsU
```

1. **Header**: `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9`
2. **Payload**: `eyJ1c2VySWQiOiIxMjM0NSIsInJvbGUiOiJhZG1pbiIsImV4cCI6MTY3NTI3NTYwMH0`
3. **Signature**: `mI4P3drROKwSxH7bEhCd2J9o7ZXLWW2dNyM6lZZgYsU`

---

### **Summary**

- **JWT**: A compact, self-contained, signed token for secure information transfer.
- **Components**: Header, Payload, Signature.
- **Uses**: Authentication, Authorization, and Information Exchange.
- **Storage**: Typically stored in localStorage or cookies.