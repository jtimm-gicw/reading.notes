# 401-Read_06

## Questions

### Securing Passwords

1. Explain to a non-technical friend how you would safely hash and store a password.
Because even you don’t want to keep the actual password written down anywhere — in case someone breaks into the vault. This scrambled version (called a hash) can’t be turned back into the original password, even by the person who created it.

**What makes it really safe:**
*Hashing*: We scramble your password with a secure method.

*Salting*: We add some extra random text (called a salt) before scrambling. This makes sure even if two people have the same password, their final scrambled versions are different.

Slow and strong hashing: We use algorithms (like bcrypt or Argon2) that take a bit longer to run — making it much harder for hackers to try lots of guesses quickly.
**In short:**
We never store your actual password. We store a scrambled version that can’t be reversed, and we add some secret sauce to make it even more secure. So even if someone steals the database, your real password stays safe.

2. What is Bcrypt?
When you create a password (like Banana123!), we don’t want to store it as-is, because if someone hacks the system, they’d see everyone’s real passwords.
So instead, we use Bcrypt to:
- **Scramble your password into a long, random-looking string (this is called a hash).**

- **Add some secret spice (a “salt”) to make each hash unique — even if two people have the same password.**

- **Blend it slowly on purpose — so it takes time to process each password. That way, if hackers try to guess a million passwords quickly, it slows them down a lot.**

3. Why might you use something like Bcrypt?
🔐 1. **To Protect Passwords**
If your app gets hacked, and you're storing plain (unscrambled) passwords, attackers can see every user's login. Bcrypt hides the real passwords by turning them into a hash — so even if someone steals your database, they can’t read the actual passwords.

🧂 2. **To Prevent Duplicate Hashes**
Bcrypt adds a random “salt” to each password before hashing. That means:
Even if two users have the same password (password123), their stored hashes will look completely different.

This protects against attacks that use precomputed lists of hashes (called rainbow tables).

🐢 3. **To Slow Down Hackers**
Bcrypt is intentionally slow — it takes a little bit of time to hash each password. That may sound bad, but it’s actually great! It means if an attacker tries to guess thousands of passwords (called a brute-force attack), each guess takes longer, making the attack much harder.

🛠️ 4. **To Follow Best Practices**
Using Bcrypt is a widely accepted security standard. It’s trusted, battle-tested, and designed for password hashing. That’s why developers use it instead of general-purpose hash tools like MD5 or SHA-1, which are fast and unsafe for passwords.


### Basic Auth

1. What is Basic Authentication?
Basic Authentication (or "Basic Auth") is a simple way for your app or browser to prove who you are when making a request to a server.
Think of it like showing your username and password to get access to a private room.
- You send your credentials (username and password) with each request.

- The server checks them and lets you in if they’re correct.

🛑 **Important:** Basic Auth is not secure on its own. It should only be used over HTTPS, so no one can see your username and password while it's being sent.

2. What properties are necessary in the header of a Basic Auth request?
When you use Basic Auth, you add a special line in the HTTP request headers, like this:
Authorization: Basic <encoded credentials>
Let’s break that down:
* Authorization is the header key.

* Basic tells the server you’re using Basic Auth.

* <encoded credentials> is your username:password combo encoded in a special format (we’ll cover that next).

✅ So the necessary property is:
Authorization: Basic <something>

3. How are username:password in Basic Auth encoded?
When you use Basic Auth, you add a special line in the HTTP request headers, like this:
Authorization: Basic <encoded credentials>
Let’s break that down:
Authorization is the header key.

Basic tells the server you’re using Basic Auth.

<encoded credentials> is your username:password combo encoded in a special format (we’ll cover that next).

✅ **So the necessary property is:**
Authorization: Basic <something>

How are username:password in Basic Auth encoded?
The username and password are put together like this:
username:password
*Example:*
`jason:mySecret123`

Then, that whole string is encoded using something called Base64.
🧠 Think of Base64 like a way of hiding something in plain sight, not strong encryption — it just changes the format to something safe to send over the internet.
*So:*
`jason:mySecret123` → `(Base64)` → `amFzb246bXlTZWNyZXQxMjM=`

Your final header would be:
**Authorization: Basic amFzb246bXlTZWNyZXQxMjM=**

The server then decodes it, splits it back into username and password, and checks if they match.
### OWASP auth cheatsheet

1. Define the authentication process to a non-technical recruiter.
**🔐 What is Authentication?**
*Authentication is how a system makes sure you are who you say you are.*
Think of it like checking someone's ID before letting them into a building.

**🧾 How It Works (in simple terms):**
*You provide credentials*
 — Usually a username and password. It's like showing your name and a badge to security.

*The system checks those credentials*
 — It compares what you entered with what it has on file (safely stored). If they match, you’re in.

*You’re given access*
 — Once you’re verified, you’re allowed into your account or the app’s private features.

**🧠 Analogy:**
Imagine you walk up to a locked door at work:
You swipe your badge (username/password).

The security system checks if your badge is valid.

*If yes*, the door unlocks. *If not*, it stays locked.

That’s authentication in a nutshell — *it's the first step in protecting accounts, data, and users.*

2. How should your error messaging respond (both HTTP and HTML)? Why?
✅ **What does "error messaging" mean?**
When something goes wrong — like a user typing the wrong password or trying to access something they shouldn’t — your app or server sends back a message. This message can appear:
*In the HTTP response (what your app or browser reads)*

*In the HTML (what the user sees on the page)*

**🧠 Why both HTTP and HTML responses matter:**
**HTTP** responses are for *developers, APIs, and frontend apps* to handle errors properly.

**HTML** (or user-facing messages) are *for actual people to understand what went wrong and how to fix it* — without giving away sensitive info.

3. Bookmark this link also and consider OWASP fundamentals any time you interact with authentication. Applications developed with security in mind from inception have fewer vulnerabilities throughout their lifecycle.
*n/a*
