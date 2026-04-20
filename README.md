# 🛡️ Phishing Website Detection using Machine Learning Techniques

## 📚 Course
ICT Risk Assessment — University of Pisa  

## 👨‍🎓 Author
Hamas Ali  
Matricola: 726267  

---

# 📌 Project Overview

Phishing is one of the most critical cybersecurity threats where attackers create fake websites to steal sensitive user information such as login credentials, banking details, and personal data.

Traditional detection techniques like blacklist and whitelist systems fail because:
- They only detect known phishing URLs
- They cannot detect newly generated phishing attacks
- They require constant manual updates

This project proposes a **Machine Learning-based phishing detection system** that can:
- Learn patterns from data
- Detect unseen phishing websites
- Provide automated and scalable security solutions

---

# 🎯 Objective

- Analyze and compare different machine learning approaches
- Study three major research papers
- Implement a phishing detection system using ML
- Evaluate multiple models and identify the best-performing one

---

# 📖 Research Papers (Detailed Study)

## 🔹 Paper 1 — ELM Based Approach
📄 https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9114695

### Approach
- Uses **Extreme Learning Machine (ELM)**
- Single hidden layer neural network
- Random input weights, analytically computed output weights

### Features Used (30 Features)
- URL-based features (length, symbols, IP usage)
- HTML/JavaScript features (iframe, popup, scripts)
- Abnormal features (redirects, unusual patterns)
- Domain features (age, DNS, traffic)

### Key Contribution
- Very fast training (no iterative backpropagation)
- Suitable for real-time detection

---

## 🔹 Paper 2 — NLP + Domain + AutoML (Advanced Approach)
📄 https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10910759

### Approach
- Combines:
  - NLP (Natural Language Processing)
  - Domain-based features (WHOIS, DNS)
  - AutoML for automatic model selection

### Feature Engineering
- NLP features:
  - Suspicious keywords
  - Grammar/spelling errors
  - Content tone
- Domain features:
  - Domain age
  - DNS records
  - Registration details

### AutoML
- Tests multiple models:
  - Random Forest
  - Gradient Boosting
  - Decision Tree
  - SVM
- Automatically selects best model

### Key Contribution
- Highest accuracy (~95.8%)
- Rich feature representation
- Automated optimization

---

## 🔹 Paper 3 — Classical ML Comparison
📄 https://scholarworks.uttyler.edu/cgi/viewcontent.cgi?article=1022&context=compsci_fac

### Approach
- Uses only **URL-based features**
- Dataset: UCI Repository

### Features (9 Features)
- URL length
- IP address presence
- Domain age
- Web traffic
- Popup window
- Request URL
- Anchor URL
- SSL state
- Server form handler

### Models Used
- Decision Tree (Best: ~91.5%)
- SVM (~86%)
- Naïve Bayes (~86%)
- Neural Network (~84%)

### Key Contribution
- Simple and lightweight system
- Demonstrates effectiveness of basic features

---

# ⚖️ Comparative Analysis

| Aspect | Paper 1 | Paper 2 | Paper 3 |
|------|--------|--------|--------|
| Features | 30 structured | NLP + Domain | 9 URL |
| Complexity | Medium | High | Low |
| Accuracy | ~90–92% | ⭐ ~95.8% | ~91.5% |
| Model Type | ELM | AutoML | Decision Tree |
| Strength | Fast | Most powerful | Simple |

---

# 🧠 Our Implementation

## 📊 Dataset
- Source: UCI Phishing Websites Dataset
- Total samples: 11,055
- Legitimate: 6,157
- Phishing: 4,898

---

## 🔍 Feature Categories (30 Features)

### 🌐 URL-based
- URL_Length
- having_IP_Address
- having_At_Symbol
- double_slash_redirecting

### 🔐 Security Features
- SSLfinal_State
- HTTPS_token
- Domain_registeration_length

### 📄 Content Features
- Request_URL
- URL_of_Anchor
- Links_in_tags
- popUpWindow
- Iframe

### 🌍 Domain Features
- age_of_domain
- DNSRecord
- web_traffic
- Google_Index
- Page_Rank

---

# ⚙️ Machine Learning Models Used

- Decision Tree  
- Random Forest ⭐  
- SVM  
- Logistic Regression  
- Naïve Bayes  
- KNN  

---

# 🔄 Pipeline

Load Dataset → Preprocess → Train/Test Split → Train Models → Evaluate → Cross Validation

---

# 📊 Results

| Model | Accuracy | Precision | Recall | F1 |
|------|--------|----------|--------|----|
| ⭐ Random Forest | 97.69% | 98.04% | 96.73% | 97.38% |
| Decision Tree | 96.97% | 97.60% | 95.51% | 96.54% |
| SVM | 95.61% | 96.33% | 93.67% | 94.98% |
| KNN | 94.71% | 94.99% | 92.96% | 93.97% |
| Logistic Regression | 92.81% | 93.44% | 90.10% | 91.74% |
| Naïve Bayes | 61.60% | 53.59% | 99.90% | 69.75% |

---

# 🔥 Key Findings

- Random Forest is the best model (highest accuracy & stability)
- SSLfinal_State is the most important feature
- Naïve Bayes fails due to feature dependency
- More features → better performance (Paper 2 proves this)

---

# 🚀 Practical Outcome

The system achieves:
- High accuracy
- Strong generalization
- Real-world applicability

---

# 📦 Project Structure

📁 phishing-detection-ml/  
┣ 📜 README.md  
┣ 📜 phishing_detection.ipynb  
┣ 📜 UCI Dataset
┣ 📜 Project Slides  

---

# ▶️ How to Run

Open notebook in the google colab and put the dataset folder in the same repository.

---

# 📎 Presentation

Slides included in repository.

---

# 📌 Future Work

- Add NLP-based feature extraction
- Integrate real-time detection system
- Use live phishing data (PhishTank)
- Implement online learning

---

# 💬 Conclusion

Machine Learning provides a powerful solution for phishing detection.  
Combining feature engineering with robust models like Random Forest enables highly accurate and scalable cybersecurity systems.
