# SAST Exercise Student Worksheet

**Student Name:** _________________________ **Date:** _____________

**Class/Section:** _______________________ **Partner(s):** _______________________

---

## 📋 Exercise 1: SAST Fundamentals

### 1.1 Tool Availability Check
```bash
# Command run:
python -c "from src.analyzer.static_analyzer import SecurityToolRunner; print(SecurityToolRunner().check_available_tools())"

# Results:
Available tools: ________________________________________________
```

### 1.2 Basic Command Understanding
Fill in what each command flag does:

| Command Flag | Purpose |
|--------------|---------|
| `--educational` | _________________________________ |
| `--verbose` | _________________________________ |
| `--output json` | _________________________________ |

### 1.3 Reflection Questions
1. **What is the main difference between SAST and DAST?**
   _________________________________________________________________
   _________________________________________________________________

2. **When in the development process should SAST be performed?**
   _________________________________________________________________

3. **What are two limitations of SAST tools?**
   a) ____________________________________________________________
   b) ____________________________________________________________

---

## 📋 Exercise 2: Flask Application Analysis

### 2.1 Initial Analysis Results
```bash
# Command run:
python src/analyzer/analyze_cli.py samples/vulnerable-flask-app --educational

# Findings Summary:
Total: _____ | Critical: _____ | High: _____ | Medium: _____ | Low: _____
```

### 2.2 Vulnerability Classification
Fill in the table with findings from your analysis:

| Vulnerability Type | Count | Highest Severity | Example Line Number |
|-------------------|--------|------------------|-------------------|
| SQL Injection | _____ | ____________ | ________________ |
| XSS | _____ | ____________ | ________________ |
| Debug Mode | _____ | ____________ | ________________ |
| Authentication Issues | _____ | ____________ | ________________ |
| Other: _____________ | _____ | ____________ | ________________ |

### 2.3 Deep Dive Analysis
Choose ONE SQL injection finding and analyze it:

**File:** _____________________________ **Line:** __________

**Vulnerable Code Snippet:**
```python
# Copy the vulnerable code here:




```

**Why is this vulnerable?**
_________________________________________________________________
_________________________________________________________________

**How could an attacker exploit this?**
_________________________________________________________________
_________________________________________________________________

**How would you fix it?**
```python
# Write your secure code here:




```

### 2.4 Risk Assessment
**What is the MOST CRITICAL vulnerability you found and why?**
_________________________________________________________________
_________________________________________________________________
_________________________________________________________________

---

## 📋 Exercise 3: PWA Application Analysis

### 3.1 Multi-File Analysis Results
```bash
# Command run:
python src/analyzer/analyze_cli.py samples/unsecure-pwa --educational

# Results:
Files Analyzed: _________ | Total Findings: _________ | Tools Used: _________
```

### 3.2 PWA-Specific Security Issues
**What PWA-specific security concerns did you identify?**
_________________________________________________________________
_________________________________________________________________

**How do PWA security considerations differ from traditional web apps?**
_________________________________________________________________
_________________________________________________________________

### 3.3 Cross-Application Comparison
| Application | Total Findings | Highest Risk Vulnerability | Overall Risk Level (1-10) |
|-------------|----------------|----------------------------|---------------------------|
| Flask App | _____________ | ______________________ | ________________________ |
| PWA App | _____________ | ______________________ | ________________________ |

**Which application has the highest security risk and why?**
_________________________________________________________________
_________________________________________________________________

---

## 📋 Exercise 4: Advanced SAST Techniques

### 4.1 JSON Analysis Exercise
```bash
# Generate JSON reports
python src/analyzer/analyze_cli.py samples/vulnerable-flask-app --output json > flask_report.json

# Count findings by severity
grep -o '"severity": "high"' flask_report.json | wc -l
```

**High severity findings count:** _____________

**What are the advantages of JSON output for security teams?**
_________________________________________________________________
_________________________________________________________________

### 4.2 Automation Potential
**How could these SAST tools be integrated into a development workflow?**
_________________________________________________________________
_________________________________________________________________

**What would be the benefits of automated security scanning?**
_________________________________________________________________
_________________________________________________________________

---

## 📋 Exercise 5: Remediation Planning

### 5.1 Priority Matrix
Create a priority matrix for the Flask application vulnerabilities:

| Vulnerability | Severity | Ease of Exploitation | Business Impact | Priority (1-5) |
|---------------|----------|---------------------|----------------|----------------|
| _____________ | ________ | __________________ | _____________ | _____________ |
| _____________ | ________ | __________________ | _____________ | _____________ |
| _____________ | ________ | __________________ | _____________ | _____________ |
| _____________ | ________ | __________________ | _____________ | _____________ |

### 5.2 Remediation Plan
**Top 3 vulnerabilities to fix first:**

1. **Vulnerability:** _____________________________________________
   **Why first:** ________________________________________________
   **How to fix:** _______________________________________________
   **Estimated effort:** _________________________________________

2. **Vulnerability:** _____________________________________________
   **Why second:** _______________________________________________
   **How to fix:** _______________________________________________
   **Estimated effort:** _________________________________________

3. **Vulnerability:** _____________________________________________
   **Why third:** ________________________________________________
   **How to fix:** _______________________________________________
   **Estimated effort:** _________________________________________

### 5.3 Fix Implementation
**Choose ONE vulnerability to actually fix. Document your process:**

**Vulnerability chosen:** ________________________________________

**Original vulnerable code:**
```python
# Paste original code here:




```

**Fixed secure code:**
```python
# Paste your fix here:




```

**Re-run analysis results after fix:**
Before: _____ findings | After: _____ findings | Improvement: _____ fewer findings

---

## 🎓 Final Reflection

### Knowledge Assessment
**1. In your own words, explain what Static Application Security Testing is:**
_________________________________________________________________
_________________________________________________________________
_________________________________________________________________

**2. What are the three most important things you learned from this exercise?**
a) ____________________________________________________________
b) ____________________________________________________________
c) ____________________________________________________________

**3. How has this exercise changed your perspective on software security?**
_________________________________________________________________
_________________________________________________________________
_________________________________________________________________

### Career Interest
**4. Which cybersecurity career path interests you most after this exercise?**
□ Application Security Engineer
□ DevSecOps Engineer  
□ Security Consultant
□ Penetration Tester
□ Other: _______________________

**Why?** _____________________________________________________
_________________________________________________________________

### Real-World Application
**5. How would you explain the importance of SAST to:**

**A software developer:**
_________________________________________________________________
_________________________________________________________________

**A business manager:**
_________________________________________________________________
_________________________________________________________________

**A friend who's not in tech:**
_________________________________________________________________
_________________________________________________________________

### Future Learning
**6. What security topics would you like to learn about next?**
□ Dynamic Application Security Testing (DAST)
□ Penetration Testing
□ Incident Response
□ Network Security
□ Cryptography
□ Other: _______________________

---

## 📊 Self-Assessment Checklist

Rate yourself on each skill (1=Beginner, 5=Expert):

| Skill | Rating (1-5) |
|-------|-------------|
| Understanding SAST concepts | _____ |
| Using security analysis tools | _____ |
| Interpreting tool outputs | _____ |
| Identifying vulnerability types | _____ |
| Planning remediation strategies | _____ |
| Communicating security findings | _____ |

**What skill do you most want to improve?**
_________________________________________________________________

**What was the most challenging part of this exercise?**
_________________________________________________________________
_________________________________________________________________

**What was the most interesting discovery you made?**
_________________________________________________________________
_________________________________________________________________

---

**🎯 Congratulations on completing the SAST exercise! You've taken an important step toward understanding application security.**

**Teacher's Comments:**
_________________________________________________________________
_________________________________________________________________
_________________________________________________________________

**Grade:** _________ **Date Completed:** _________________