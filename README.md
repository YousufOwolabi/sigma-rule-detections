# Sigma Rule Detections

🚀 **Author:** Yousuf Owolabi  
🔍 **Role:** Security Analyst | SOC Analyst | Detection Engineer  

---

## 💡 About This Repository

This repository contains custom Sigma rules and Python scripts for detection engineering. Sigma rules allow you to write **generic detections** for security events, which can be converted into queries for SIEMs like Splunk, ElasticSearch, and others.

---

## 📁 Contents

### ✅ Sigma Rules

- `suspicious_cronjob.yml`  
    → Detects suspicious cron jobs executing tools like:
    - wget
    - curl
    - nc
    - bash reverse shells

### ✅ Python Scripts

- `convert.py`  
    → Converts Sigma rules into Splunk queries using pySigma.

Example converted Splunk query:

Command IN ("*wget*", "*curl*", "*nc*", "*bash -i*")


---

## ⚙️ How to Use

### Convert Sigma Rule to Splunk Query

Activate your virtual environment:

```bash
source ~/sigma-rules-Ghost/sigma-env/bin/activate

Run the Python converter script:

python convert.py
