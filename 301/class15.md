# 301-Read_15

## What is OAuth

1. What is OAuth?
OAuth (Open Authorization) is a secure way for apps and websites to access your information from other services (like Google, Facebook, or GitHub) without needing your password.

2. Give an example of what using OAuth would look like.
Imagine you’re building a fitness app called FitTracker that allows users to log in using their Google account. 

3. How does OAuth work? What are the steps that it takes to authenticate the user?
**STEP 1:** Request Access (Knocking on the Door):
 You click a button like "Log in with Google" on an app, letting it know you want to use your Google account.


**STEP 2:** Redirect to the Gatekeeper:
 The app sends you to Google, the service that controls your data, to confirm your identity.


**STEP 3:** Check Your ID (Consent):
 Google asks you to confirm if you really want to share your information and tells you exactly what data the app will see (like your name, email, and profile picture).


**STEP 4:** Permission Granted (Getting the Pass):
 If you agree, Google gives your app a special one-time code that acts like a temporary hall pass.


**STEP 5:** Trade for a Key:
 Your app takes that code back to Google and exchanges it for a more powerful, longer-lasting access token – like a backstage pass that lets it interact with your data.


**STEP 6:** Access Your Data (VIP Access):
 With this token, the app can now fetch your data as long as the token remains valid, without ever needing your password.


**STEP 7:** Token Expiry (Bouncer’s Watch):
 The token eventually expires or can be revoked, ensuring long-term security.

4. What is OpenID?
OpenID is like a digital ID card that lets you prove who you are when logging into different websites without needing a separate password for each one.

## Authorization and Authentication flows

1. What is the difference between authorization and authentication?
- **Authentication** (Proving Who You Are)
Think of this like showing your ID at the door of a nightclub.
It’s about confirming your identity – making sure you are who you say you are.

*Examples:* Entering a password, scanning a fingerprint, or using facial recognition.

- **Authorization** (What You’re Allowed to Do)
Once you’re inside, this is like having a VIP wristband.
It’s about what you’re allowed to access or do now that your identity is confirmed.


*Examples:* Accessing certain sections of a website, editing settings, or managing other users.

2. What is Authorization Code Flow?
The Authorization Code Flow is a secure way for web apps to let users log in using their existing accounts (like Google, GitHub, or Facebook) without sharing their passwords. It’s a key part of OAuth 2.0 and is designed for server-side apps.

3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
PKCE (Proof Key for Code Exchange) is an extra layer of security added to the standard Authorization Code Flow in OAuth 2.0. It’s designed mainly for mobile and single-page apps, which can’t keep secrets as securely as server-based apps.

4. What is Implicit Flow with Form Post?
The Implicit Flow with Form Post is an OAuth 2.0 flow designed for single-page apps (SPAs) and other clients that can’t securely store secrets. It’s a variation of the Implicit Flow but with a bit more security.

5. What is Client Credentials Flow?
The Client Credentials Flow is an OAuth 2.0 flow for apps that need to authenticate themselves, not a user. It’s mainly used for machine-to-machine (M2M) communication or server-to-server interactions.

6. What is Device Authorization Flow?
The Device Authorization Flow is a special OAuth 2.0 flow designed for devices with limited input capabilities (like smart TVs, gaming consoles, or IoT devices) that can't easily prompt the user for a username and password. It allows the user to log in using a separate device (like a phone or computer).

7. What is Resource Owner Password Flow?
The Resource Owner Password Flow is an OAuth 2.0 authentication method where a user provides their username and password directly to an app (rather than being redirected to a login page) to gain access to protected resources. This flow is generally used for apps that trust the user (like mobile apps or apps with high user confidence), but it’s less secure than other OAuth flows and is not recommended for most use cases.
