# 401-Read_07

## Questions
### Intro to JWT

1. What is a JSON Web Token (JWT)?
A JSON Web Token (JWT) is a compact, URL-safe way of representing claims between two parties. It's commonly used for authentication and authorization in web applications.
 
2. When should we use JSON Web Tokens?
You should use JSON Web Tokens (JWTs) when you need a compact, secure way to transmit user identity or claims between parties, especially in stateless authentication systems.

3. Claims are expected in which structural component of a JWT?
Claims are expected in the *payload* component of a JWT.

### Are JWTs Secure?

1. If I get a JWT and I can decode the payload, how can we call that secure?
 Yes, you can decode the JWT payload — and that’s expected.
JWTs are base64Url-encoded, not encrypted. So:
- Anyone who has the token can decode the payload.
- But they cannot trust or change it without access to the secret key used to sign it.

2. If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.
If sending a JWT, both the sender and the receiver must know the:
🔐 **Secret key** (for HMAC)
or
🔐 **Public/Private key pair** (for RSA/ECDSA)

3. Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.
When one system (the sender) needs to send information (like user data) to another system (the receiver) securely, it wraps up that information with a special seal or signature.
That seal is created by combining:
- The **message itself** (what’s being said),
- A **shared secret code** that only the sender and receiver know.

## Videos

### JWTs Explained

1. Why use JWT?
Because it lets websites and apps know who you are — securely and without needing to remember you on the server.

2. JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.
Think of a JWT like a digital passport that fits in your pocket (compact) and holds all the info you need to get through airport security (self-contained).
🧩 Compact means:
- It’s small and easy to carry.
- You can send it quickly — even over slow networks or in a web link.

3. What are the three components (the structure) of a JWT signature?
A **JSON Web Token** (JWT) consists of three components, joined by periods (.), like so:
<Header>.<Payload>.<Signature>


### Bookmark and Review
* npm jsonwebtoken docs

### Reflection
1. What are your learning goals after reading and reviewing the class README?
I want to know more about when to use Basic or Bearer Authentication

