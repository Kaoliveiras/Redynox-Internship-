# Task 2: Web Application Security

## 📌 Objective
Learn about common web application vulnerabilities by analysing a simple web application.

---

## 1. Setup

### Java Environment
- Java version verified using `java -version`

### WebGoat Installation
WebGoat is an intentionally vulnerable web application maintained by OWASP for learning purposes.

**Steps taken:**
1. Downloaded WebGoat 2023.8 from the official GitHub repository
2. Ran WebGoat using the command: `java -jar webgoat-2023.8.jar`
3. Accessed WebGoat at `http://localhost:8080/WebGoat`
4. Created an account to start the lessons

---

## 2. Vulnerability Analysis

### SQL Injection
**Description:** SQL Injection occurs when user input is improperly sanitized and inserted directly into SQL queries.

**Manual Exploitation:**
1. Navigated to the SQL Injection lesson
2. Entered: `'; DROP TABLE access_log; --` as the search string
3. Successfully deleted the access_log table

**Why it's dangerous:**
- Attackers can bypass authentication
- Can extract sensitive data
- Can modify or delete database records

---

### Cross-Site Scripting (XSS)
**Description:** XSS allows attackers to inject malicious scripts into web pages.

**Manual Exploitation:**
1. Used the browser console to execute JavaScript
2. Entered: `alert('XSS Test')` in the console
3. The script executed, proving the vulnerability

**Why it's dangerous:**
- Steal session cookies
- Deface websites
- Redirect users to malicious sites

---

### Cross-Site Request Forgery (CSRF)
**Description:** CSRF tricks authenticated users into executing unwanted actions.

**Manual Exploitation:**
1. Created an HTML file with a hidden form
2. Form submitted a request to change data
3. Successfully executed the CSRF attack and obtained a flag

**Why it's dangerous:**
- Change user credentials
- Perform unauthorized transactions
- Modify account settings

---

## 3. Mitigation Recommendations

| Vulnerability | Mitigation Steps |
|---------------|------------------|
| **SQL Injection** | Use parameterized queries, input validation, least privilege accounts |
| **XSS** | Output encoding, Content Security Policy (CSP), HTTPOnly cookies |
| **CSRF** | Implement anti-CSRF tokens, SameSite cookies, re-authentication |

---

## 4. Reflection

### Web Security Best Practices

In a real-world production environment, additional measures would include:

1. **Secure Development Lifecycle:** Security testing from the start of development
2. **Regular Security Training:** Developers trained on secure coding practices
3. **Web Application Firewall (WAF):** Additional layer of protection
4. **Regular Penetration Testing:** Professional security assessments

---

## ✅ Task Completion Status

- [x] Java environment verified
- [x] WebGoat installed and configured
- [x] SQL Injection identified and exploited
- [x] XSS identified and exploited
- [x] CSRF identified and exploited
- [x] Documentation complete
