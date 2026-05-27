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

site:vulnweb.com intitle:"login"

<img width="714" height="424" alt="Image" src="https://github.com/user-attachments/assets/f7da8dd3-a66d-4a57-9b6a-cd31d56d9b4d" />

### 🔎 Find Admin Panels

inurl:admin login

<img width="676" height="601" alt="Image" src="https://github.com/user-attachments/assets/a5823dd2-853d-4790-8022-6a4433a02720" />

### 🔎 Find Exposed Documents

site:hackthissite.org filetype:pdf

<img width="697" height="634" alt="Image" src="https://github.com/user-attachments/assets/f8da9636-027f-4d97-a338-97e623a446df" />

### 🔎 Find Open Directories

intitle:"index of" "parent directory"

<img width="712" height="611" alt="Image" src="https://github.com/user-attachments/assets/e398679a-8b8c-4759-9c75-5574dfd04ffd" />

### 🔎 Find Configuration Files

filetype:env DB_PASSWORD

<img width="681" height="567" alt="Image" src="https://github.com/user-attachments/assets/a8adb252-ac31-48fe-a4f3-83f92bc73e5d" />
