# 🚀 **DevBuddy: AI Code Review Service (Open Source)**
> DevBuddy: AI Code Review Service (Open Source)

| **[Korean](README.md)** | **[English](README_ENG.md)** |

---

## 🎯 **Introduction**
🤖 **DevBuddy** is an **AI-powered automated code review service** designed for solo developers.  
Whenever you push your code, it automatically reviews it, suggests improvements, and **generates unit tests** to help developers focus on creative tasks! 🎨✨

🚀 The **initial version is open-source**, and the **cloud version** will provide additional features such as notifications, automation of repetitive tasks, and enhanced security.

---

## 🛠 **Features**

### 📌 **Core Features (Open Source)**
- **Automated Code Review**:  
  AI analyzes code style, bug risks, and security vulnerabilities.
- **Improvement Suggestions**:  
  Recommends performance optimization and refactoring.
- **Automated Unit Test Generation**:  
  AI analyzes functions and generates test cases.
- **Code Documentation & Explanation**:  
  Automatically generates documentation and explanations.
- **Git Integration**:  
  Adds **automated PR reviews and comments** on GitHub/GitLab.
- **CLI & API Support**:  
  Can be executed **locally**.

---

### ☁️ **Cloud Version (Upcoming)**
- **Notification System**:  
  Delivers review results via **email, Slack**, etc.
- **Automation of Repetitive Tasks**:  
  Executes **auto-refactoring** based on defined criteria.
- **Enhanced Security Analysis**:  
  Detects library vulnerabilities and **recommends updates**.
- **Dashboard**:  
  Manages **code quality** and **review history** per project.

---

## 🚀 **Installation & Execution**

### 1️⃣ **Running Locally**
```bash
git clone https://github.com/your-repo/code-review-ai.git
cd code-review-ai
pip install -r requirements.txt
python main.py
```

---

### 2️⃣ **Running in GitHub Actions**
Add the `.github/workflows/code-review.yml` file:
```yaml
name: Code Review AI
on:
  pull_request:
    types: [opened, synchronize]
jobs:
  review:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v3
      - name: Run AI Code Review
        run: |
          curl -X POST -H "Authorization: Bearer ${{ secrets.API_KEY }}" \ 
               -d '{"repo": "${{ github.repository }}", "pr": "${{ github.event.pull_request.number }}"}' \ 
               https://api.codereviewai.com/review
```

---

## ✅ **How to Contribute**
1. **Check Issues:** Select a task to work on.  
2. **Create a Branch:** Create a `feature-branch` and start development.  
3. **Submit a PR:** Send a code review request.  
4. **Merge:** After review, changes will be merged.


### 🛠 **Development Stack**
- **Backend:** FastAPI, Celery  
- **AI Models:** GPT-4, Claude, Mistral  
- **Database:** PostgreSQL, Redis  
- **Deployment:** Docker, Kubernetes  
- **Testing:** pytest, Jest  


### 🎯 **Contributor Roles**
- **Core Developer:** AI optimization, backend development, performance enhancements.  
- **Frontend Developer:** Web dashboard and VS Code extension development.  
- **Tester:** Automated testing and code reviews.  
- **Documentation Specialist:** Writing README, tutorials, API documentation.  
- **Community Manager:** Managing issues, answering questions, improving contribution guidelines.  
- **UI/UX Designer:** Improving usability and interface design.  

👉 **How to Apply:** Check the "Manager Recruitment" label on [GitHub Issues](https://github.com/your-repo/devbuddy/issues)!

---

## 🛠 **Competitor Services and Feature Comparison**

| **Service Name**          | **Launch Date** | **Open Source**         | **GitHub Repository**                                                   | **Active Status**          | **Key Features**                                                                    | **Target Users**                          | **Distinguishing Features**                                      |
|-----------------------|-------------|---------------------|---------------------------------------------------------------------|------------------------|---------------------------------------------------------------------------------|---------------------------------------|---------------------------------------------------------------|
| **DevBuddy**          | 2025        | ✅ Yes              | [DevBuddy GitHub](https://github.com/your-repo/devbuddy)            | Active                 | AI code review, automated test generation, documentation, GitHub Actions support | Solo developers, startups            | User-friendly UI, tailored for solo developers                |
| **Codacy**            | 2014        | ✅ Partial          | [Codacy GitHub](https://github.com/codacy)                          | Active                 | Code analysis, security checks, test automation                                  | Enterprises, teams                   | Focus on security and quality                                |
| **DeepCode**          | 2019        | ✅ Yes              | [DeepCode GitHub](https://github.com/DeepCodeAI)                    | Integrated into Snyk   | AI-based code review, static analysis                                            | Developers, open-source projects     | Machine learning-driven static analysis                       |
| **SonarQube**         | 2007        | ✅ Yes              | [SonarQube GitHub](https://github.com/SonarSource/sonarqube)        | Active                 | Code quality and security analysis                                               | Enterprises, large-scale projects    | Comprehensive large-scale solution                            |
| **GitHub Copilot**    | 2021        | ❌ No               | N/A                                                                 | Active                 | AI code autocompletion, some code review capabilities                            | All developers                       | Real-time code autocompletion                                |
---

## 📝 **License**
This project is **licensed under the MIT License**.  

🔹 **What is MIT License?**
> The MIT License is a permissive open-source license that allows anyone to use, modify, and distribute the software with minimal restrictions.
It is widely used in open-source projects because it provides flexibility and encourages collaboration.
All you need to do is include the original license notice when redistributing the code.

---

## Community & Support
- 💬 [**Discord Channel**](https://discord.gg/7bSqAjPZDe)
- 📧 **Email: support@baryon.ai**
- 📝 [**Contribution Guide**](CONTRIBUTING.md)

---
🚀 **Join us in building the AI-powered code review ecosystem!**

