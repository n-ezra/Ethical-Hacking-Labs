# 🔍 Search Engine Reconnaissance (Google Dorking)

## 📌 Overview
Search Engine Reconnaissance, also known as **Google Dorking**, is a passive information gathering technique used to discover publicly available sensitive information using advanced search queries.

It is an essential part of the **reconnaissance phase** in penetration testing.

---

## ⚠️ Disclaimer
> This project is for educational purposes only.  
> Do not perform these techniques on unauthorized systems. Always follow ethical hacking and legal guidelines.

---

## 🧠 What is Google Dorking?
Google Dorking uses advanced search operators to filter search results and find specific types of information indexed by search engines.

---

## 🛠️ Google Dork Operators

| Operator   | Description                        | Example                     |
|------------|----------------------------------|-----------------------------|
| site:      | Search within a domain           | site:example.com           |
| intitle:   | Search in page title             | intitle:"login"            |
| inurl:     | Search in URL                    | inurl:admin                |
| filetype:  | Search specific file types       | filetype:pdf               |
| cache:     | View cached version of a page    | cache:example.com          |

---

## 🎯 Practical Examples

### 🔎 Find Login Pages
```bash
site:vulnweb.com intitle:"login"

<img width="714" height="424" alt="Image" src="https://github.com/user-attachments/assets/f7da8dd3-a66d-4a57-9b6a-cd31d56d9b4d" />
