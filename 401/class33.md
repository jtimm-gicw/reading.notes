# React Cookies & RBAC - Notes

## 1. What is Role-Based Access Control (RBAC)?
- **Definition:** RBAC controls *who can do what* by assigning permissions based on **roles**.
- **Roles act like job titles** – they group permissions together (Admin, Editor, Viewer).
- **Key idea:** Users get a role → the role decides what actions they can perform.
- Saves time, avoids mistakes by not assigning permissions one-by-one.

---

## 2. Example of RBAC with CRUD Operations

| **Role**  | **Create** | **Read** | **Update** | **Delete** |
|-----------|-----------|---------|-----------|-----------|
| **Admin** |     ✅    |    ✅  |    ✅    |   ✅      |
| **Editor** |    ✅    |    ✅  |    ✅    |   ❌      |
| **Viewer** |    ❌    |    ✅  |    ❌    |   ❌      |

- **Admin:** Full control (create, read, update, delete)
- **Editor:** Can create & edit but not delete
- **Viewer:** Can only read

---

## 3. Benefits of RBAC
- **Security:** Prevents unauthorized access.
- **Consistency:** Manage permissions by role, not per user.
- **Scalability:** Easy to add new users.
- **Compliance:** Helps meet security/legal rules.
- **Less error-prone:** Avoids mistakes from manual permission management.

---

## 4. Describe some `react-cookie` features
- **Manages cookies easily** in React apps.
- **Hook support:** `useCookies` for state-like usage.
- **SSR support:** Works with server-side rendering (e.g., Next.js).
- **Automatic re-rendering** when cookies change.
- **Custom options:** expiry, path, secure flags.

---

## 5. Describe some `react-cookies` features
- Function-based API: `load()`, `save()`, `remove()`.
- Works both client and server side (universal apps).
- Can store JSON objects (not just strings).
- Requires **manual updates** (not hook-based).

---

## 6. Which library would you prefer? Why?
- **Preferred:** `react-cookie`
- **Reasons:**
  - Hook-based → feels natural in modern React.
  - Components auto-update when cookies change.
  - Great for SSR (Next.js, Remix).
  - TypeScript support & active maintenance.
- **Use `react-cookies` only if:** You want a minimal, function-only API and don't need reactivity.

---

## Comparison Table

| Feature | react-cookie | react-cookies |
|--------|-------------|---------------|
| **API Style** | Hook-based (`useCookies`) | Function-based (`load`, `save`, `remove`) |
| **React Integration** | Reactive: Components re-render when cookies change | Manual: Must handle updates yourself |
| **SSR Support** | Built-in `<CookiesProvider>` for SSR | Can work but requires more setup |
| **TypeScript** | Supported | Limited |
| **Maintenance** | Actively maintained | Unmaintained |
| **Ease of Use** | Best for modern React apps | Simpler, but less "React-friendly" |
