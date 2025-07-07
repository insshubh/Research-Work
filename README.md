# 🔬 Research Work

## Optimizing the Enhanced Euclidean Algorithm: Advanced GCD Computation and Its Implications for Cryptography and Networking

### 👨‍💻 Author
- **Name:** Shubham Kumar  
- **Email:** insshubh22@gmail.com  
- **Affiliation:** Amity University, Patna

---

# 🚀 Project Repository: DLT GPT & Advanced GCD

Welcome to the combined repository for two AI and algorithm-based projects:

1. **DLT GPT** – An AI-powered chatbot for TRAI DLT Compliance Automation.  
2. **Advanced GCD** – An optimized, modular implementation of the Greatest Common Divisor for large-scale computations.

---

## 🔮 Project 1: DLT GPT – AI-Powered Chatbot for TRAI DLT Compliance

### 📌 What is DLT GPT?
DLT GPT is an intelligent chatbot that assists businesses in complying with the **Telecom Regulatory Authority of India (TRAI)**’s **Distributed Ledger Technology (DLT)** requirements. It automates the generation, validation, and formatting of SMS/WhatsApp templates according to TRAI standards.

### 🎯 Why DLT GPT?
Manual DLT compliance is error-prone and time-consuming. DLT GPT:
- Detects and fixes template formatting issues
- Converts messages to Meta-approved JSON formats
- Reduces template rejection rates
- Automates interactions with DLT portals

### 🔧 Features
- Gemini & LLaMA-based NLP engine for compliance logic
- Real-time chatbot interface (Flask)
- MongoDB database for template tracking
- WhatsApp JSON generator
- Auto-validation against TRAI rules

### 🛠️ Tech Stack
- Python, Flask, HTML/CSS
- Gemini API + LLaMA (NLP)
- MongoDB (NoSQL)
- Meta WhatsApp Business API
- AWS (for hosting)

### 🚀 Setup Instructions
```bash
git clone https://github.com/yourusername/dlt-gpt.git
cd dlt-gpt
pip install -r requirements.txt
python app.py
```

# Project Advace GCD 

## 📄 Abstract

This research introduces an enhanced version of the classical Euclidean Algorithm to compute the **Greatest Common Divisor (GCD)**. The algorithm incorporates logic to handle **zero and negative integers**, improves runtime predictability, and enhances robustness in edge cases.

The refined approach is benchmarked for cryptographic use and network routing scenarios, where modular arithmetic plays a critical role. The goal is to offer a **faster, edge-case-tolerant, and cryptography-ready** GCD mechanism.

---

## 📌 Introduction

GCD operations form the mathematical backbone for systems in **cryptography**, **digital security**, and **number theory**. This project presents an upgraded GCD algorithm designed to overcome inefficiencies of the classical method, especially for large or unusual inputs (e.g., zero or negatives).

---

## 🧠 Methodology

The enhancement introduces:
- **Absolute value normalization** for negatives
- Direct early return if either number is 0 or a clean multiple
- Iterative subtraction fallback (classic step-wise method)

### 🧾 Algorithm (C++)
```cpp
int calc_gcd (int n, int m) {
    if (n == 0) return abs(m);
    if (m == 0) return abs(n);
    n = abs(n); m = abs(m);
    int x;
    if (n % m == 0 || m % n == 0) return min(n, m);
    x = (m < n) ? n % m : m % n;
    if (n % x == 0 && m % x == 0) return x;
    while (n != m) {
        (n > m) ? n -= m : m -= n;
    }
    return n;
}
```

## ⏱️ Time Complexity

| **Case**  | **Time Complexity**       | **Notes**                                      |
|-----------|---------------------------|------------------------------------------------|
| Best      | O(1)                      | When either `n` or `m` is zero or a multiple   |
| Average   | O(log(min(n, m)))         | Logarithmic reduction via modulus              |
| Worst     | O(log(min(n, m)))         | Large co-prime numbers                         |

> ⚙️ The improvements do not alter time complexity but offer **better practical runtime** by handling edge cases early.

---

## 📡 Application in Networking and Cryptography

- **Cryptography:**  
  Used in RSA, modular inverses, and cryptographic key generation.

- **Networking:**  
  Helps in load balancing, encryption schemes, and packet scheduling.

✅ Enhances both **reliability** and **throughput** in distributed and real-time systems.

---

## 📊 Results

Empirical testing across diverse input sets (positive, zero, and negative integers) validated:

- ✅ High accuracy of results  
- ⚡ Faster average runtime  
- 🛡️ Resilient to invalid or edge-case inputs

---

## 🧩 Discussion

This enhanced GCD algorithm holds **practical significance** across a range of computational domains:

- In **cryptographic systems**, it enables secure, fast, and reliable operations.
- In **network routing and load balancing**, it aids in deterministic scheduling and resource optimization.

💡 It strengthens fundamental math logic by embedding **robust edge-case handling**, making it suitable for modern computing and security environments.

