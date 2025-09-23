# API & Auth Server Review Notes

These notes explain key concepts in simple, human language to help understand API server builds and authentication server builds.

---

## **Review API Server Build**

### **1. Difference Between a Query String Parameter and a Path Parameter**

- **Path Parameter**
  - Part of the **URL path** (like `/stuff/123`).
  - Used to identify a **specific resource**.
  - Example: `/users/45` → means “get user with ID 45.”

- **Query String Parameter**
  - Comes **after the `?`** in the URL.
  - Used for **filtering, sorting, or extra info**.
  - Example: `/users?role=admin&active=true` → means “get all users where role=admin and active=true.”

**Easy way to remember:**  
- Path parameters = **"who/what"** you want.  
- Query parameters = **"how/which way"** you want it.

---

### **2. API URL with a Path ID Parameter**

Given:  
- Domain: `http://our-site.com`  
- Version: `v3`  
- Model: `stuff`  
- ID: `things`  

**Resulting URL:**


---

### **3. Explaining a Dynamic API Interface (Non-Technical)**

- Think of an **interface** like a **menu at a restaurant**.  
- You don’t go to the kitchen; you just tell the waiter what you want from the menu.  
- The API interface works the same way:  
  - You send it a request (like ordering food).  
  - It goes to the kitchen (server), gets the result, and brings it back.  
- A **dynamic interface** means the menu can change — you can order new things or different combinations without rewriting the whole system.

---

## **Review Auth Server Build**

### **1. Using Middleware for Basic and Bearer Auth**

- **Middleware** = Code that runs before your main route.

- **Basic Auth**
  - Middleware checks username/password from the request.
  - If valid → lets you through.
  - If not → blocks you.

- **Bearer Auth**
  - Middleware looks for a token (usually in the header).
  - It verifies the token (like checking an ID card).
  - If token is good → grants access.

---

### **2. OAuth Handshake (Simplified)**

- Like logging in with Google/Facebook.  

**Steps:**
1. You click “Login with Google.”
2. Your app sends you to Google → Google asks for permission.
3. You approve → Google sends back a **temporary code**.
4. Your server exchanges that code for a **token**.
5. That token proves who you are whenever you talk to the server.

---

### **3. Role-Based Access Control (RBAC) (Non-Technical)**

- Think of it like **security badges at work**.  
- Your badge (role) decides where you can go:
  - Basic employee badge → main office only.
  - Manager badge → office + conference room.
  - Admin badge → everywhere.
- In software, your **role** determines which actions you’re allowed to do (read, write, delete, etc.).

---
