### **What is Authorization?**

**Authorization** is the process of determining what actions, resources, or data a user is allowed to access after they have been authenticated. It ensures that users only have permissions relevant to their role or identity.

---

### **Key Elements of Authorization**

1. **Access Control**: Determines what a user can do within the system.
2. **Roles & Permissions**:
    - **Role-Based Access Control (RBAC)**: Users are assigned roles, and each role has predefined permissions (e.g., "Admin," "User").
    - **Permission-Based Access Control**: Specific permissions are granted to users or roles (e.g., "read-only," "edit").
3. **Resource Protection**: Ensures users access only the data or operations they are authorized for.

---

### **Authorization vs. Authentication**

- **Authentication**: Confirms _who you are_ (e.g., logging in with credentials).
- **Authorization**: Confirms _what you are allowed to do_ (e.g., accessing specific files or settings).

---

### **Types of Authorization**

1. **Role-Based Authorization**:
    - Assigns permissions based on user roles.
    - Example: Only admins can delete a database entry.
2. **Policy-Based Authorization**:
    - Uses conditions or rules to grant access.
    - Example: A user can access a resource only during working hours.
3. **Resource-Based Authorization**:
    - Permissions are tied directly to specific resources.
    - Example: A user can edit only their own blog posts.
4. **Token-Based Authorization**:
    - Users provide a token (e.g., JWT) to prove access rights.
    - Example: API authorization.

---

### **How Authorization Works**

1. **Authentication First**: The user logs in, verifying their identity.
2. **Role/Permission Check**:
    - The system matches the user to their assigned roles or permissions.
3. **Access Decision**:
    - The system allows or denies access based on defined rules.

---

### **Common Authorization Tools & Protocols**

1. **OAuth 2.0**:
    - Grants permissions to third-party apps to act on behalf of a user (e.g., "Allow Spotify to access your Google account").
2. **RBAC Systems**:
    - Widely used in enterprise applications.
3. **JWT (JSON Web Token)**:
    - Contains encoded data about user roles and permissions.
4. **SAML (Security Assertion Markup Language)**:
    - Used in Single Sign-On (SSO) for enterprises.
5. **API Authorization**:
    - Validates whether a user or system can access specific endpoints.

---

### **Importance of Authorization**

1. **Data Security**:
    - Protects sensitive information from unauthorized users.
2. **Prevents Misuse**:
    - Limits actions users can take to their intended scope.
3. **Compliance**:
    - Ensures systems meet regulatory requirements (e.g., HIPAA, GDPR).
4. **Granular Control**:
    - Fine-tunes access for complex systems and multiple user roles.

---

### **Examples**

1. **Social Media**:
    - A regular user can edit only their profile, while an admin can manage all user accounts.
2. **E-commerce**:
    - Customers can view and purchase items, but store managers can manage inventory.
3. **APIs**:
    - A token-based API may allow reading data but not writing or deleting it unless authorized.

---

### **Conclusion**

Authorization is an essential component of secure systems. It works hand-in-hand with authentication to ensure that users or applications can only access or perform tasks that align with their roles or permissions, protecting data and maintaining compliance.