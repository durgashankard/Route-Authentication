# Route-Authentication


# 🔐 Route Authentication in React (Using Cookies)

![React](https://img.shields.io/badge/React-18-blue?logo=react)
![Cookies](https://img.shields.io/badge/Cookies-Authentication-yellow)
![Status](https://img.shields.io/badge/Project-Ready-brightgreen)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 Overview

**Route Authentication** is the process of verifying user credentials before allowing access to specific routes in a React application.

It ensures that only authorized users can access protected pages like dashboards, profiles, etc.

---

## 🔑 Key Concepts

### ✅ Authentication

* Authentication is the process of **verifying user identity**
* It checks whether the user is valid or not

👉 Methods:

* User ID & Password
* Security Token (JWT)
* Biometric Verification

---

### 🔒 Authorization

* Authorization is the process of **restricting access**
* It defines **what resources a user can access**

---

## 🍪 Route Authentication Using Cookies

Cookies are used to **store user session data** in the browser.

---

## ⚙️ Installation

```bash
npm install react-cookie --save
```

---

## 📥 Import Hook

```javascript
import { useCookies } from "react-cookie";
```

---

## 🔁 useCookies() Hook

It returns **3 important references**:

| Function   | Description         |
| ---------- | ------------------- |
| 🟢 Getter  | Access cookie value |
| 🔵 Setter  | Store cookie        |
| 🔴 Remover | Delete cookie       |

---

## 🧩 Syntax

```javascript
const [cookies, setCookie, removeCookie] = useCookies(['name']);
```

---

## 🔍 Access Cookie

```javascript
cookies['name'];
```

---

## 💾 Set Cookie

```javascript
setCookie('name', value, { expires: date_time });
```

---

## ❌ Remove Cookie

```javascript
removeCookie('name');
```

---

## ⚠️ Important Note

If `expires` is **not defined**, the cookie will automatically delete when the browser closes.

---

## 🏗️ Cookies Provider Setup

```javascript
import { CookiesProvider } from "react-cookie";

<CookiesProvider>
    <App />
</CookiesProvider>
```

---

## 🔐 Protected Route Example

```javascript
if (!cookies['user']) {
    return <Navigate to="/login" />;
}
```

---

## 📊 Summary

| Feature         | Description          |
| --------------- | -------------------- |
| Authentication  | Verify identity      |
| Authorization   | Restrict access      |
| Cookies         | Store session        |
| useCookies      | Manage cookies       |
| CookiesProvider | Global cookie access |

---

## 🚀 Conclusion

Using cookies in React helps:

* Maintain user sessions
* Protect routes
* Improve user experience

---

## 💡 Bonus Tips

* Use **JWT (JSON Web Tokens)** for better security
* Use **httpOnly & secure cookies**
* Always validate authentication on backend

---

## 👨‍💻 Author

**Durgashankar Dangi**

---

⭐ If you like this project, don’t forget to **star the repo!**
