# URL XSS & SQL Injection Scanner

A lightweight educational scanner that checks URLs for potential **XSS** and **SQL Injection** vulnerabilities by injecting payloads into query parameters and analyzing server responses.

> ⚠️ For educational and legal security testing only.  
> Do not scan websites you do not own or do not have permission to test.

---

## 🔥 Features

- Detects reflected **XSS**
- Detects basic **SQL Injection**
- No external table libraries required
- ASCII table output
- Clean code, easy to understand
- No extra dependencies except `requests`

---

## 📦 Requirements

- **Python 3.7+**
- **requests** module  

Install requests with:

```bash
pip install requests
```

---

## 🚀 Usage

Run the scanner:

```bash
python scanner.py
```

Enter a target URL:

```
Target URL: https://example.com/page.php?id=1
```

The URL must contain query parameters, for example:

- `?id=1`
- `?search=test`
- `?id=10&cat=5`

---

## 📊 Example Output

```
+------+-----------+--------------------------------------------------------+
| Type | Parameter | URL                                                    |
+------+-----------+--------------------------------------------------------+
| XSS  | search    | https://test.com/?search=<script>alert(1)</script>     |
+------+-----------+--------------------------------------------------------+
```

If nothing is found:

```
No potential vulnerabilities found.
```

---

## 🧪 Testing Targets (Safe & Legal)

You can test the scanner on intentionally vulnerable websites:

### XSS:
```
https://xss-game.appspot.com/level1/frame?query=test
```

### SQLi/XSS:
```
http://testphp.vulnweb.com/listproducts.php?cat=1
```

---

## 📁 Project Structure

```
.
├── scanner.py
└── README.md
```

---

## ⚠ Legal Disclaimer

This tool is created for **educational purposes only**.  
Do not use it for unauthorized testing.  
The author is not responsible for misuse.

---

## ⭐ Want more features?

Possible upcoming improvements:

- Multi-threading
- More payload categories
- POST request scanning
- SQL error fingerprinting
- JSON output mode
- Saving results to a file

PRs are welcome!

