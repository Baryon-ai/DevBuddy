# 🚀 DevBuddy: AI Code Review Service (Open Source) 
DevBuddy: AI 코드 리뷰 서비스 (오픈소스)

## 🎯 Introduction | 소개
🤖 DevBuddy is an AI-powered automated code review service designed for solo developers.
Whenever you push your code, DevBuddy reviews it, suggests improvements, generates unit tests, and helps you focus on creativity! 🎨✨

🤖 DevBuddy는 1인 개발자를 위한 AI 기반 자동 코드 리뷰 서비스입니다.
코드를 푸시하면 DevBuddy가 자동으로 리뷰하고, 개선 아이디어를 제공하며, 단위 테스트를 생성하여 개발자가 더 창의적인 작업에 집중할 수 있도록 도와줍니다! 🎨✨

🚀 The initial version is open-source, while the cloud version will offer advanced features like notifications, automation, and security enhancements.

🚀 초기 버전은 오픈소스로 제공되며, 클라우드 버전에서는 추가 기능(알림, 반복 작업, 보안 강화 등)이 제공될 예정입니다.


## 🛠 Features | 기능

### 📌 Core Features (Open Source) | 기본 기능 (오픈소스)
- **Automated Code Review**: AI analyzes code style, bug risks, and security vulnerabilities.
- **Improvement Suggestions**: Provides performance optimization and refactoring recommendations.
- **Automated Unit Test Generation**: AI analyzes functions and generates test cases.
- **Code Documentation & Explanation**: Automatically generates documentation and explanations.
- **Git Integration**: Adds automated PR reviews and comments for GitHub/GitLab.
- **CLI & API Support**: Can be executed locally.

- **자동 코드 리뷰**: AI가 코드 스타일, 버그 가능성, 보안 취약점 분석
- **개선 아이디어 제공**: 성능 최적화, 리팩토링 제안
- **자동 단위 테스트 생성**: AI가 함수 분석 후 테스트 코드 작성
- **코드 설명 및 문서화**: 코드 자동 분석 및 문서 생성
- **Git 연동**: GitHub/GitLab PR 자동 리뷰 및 코멘트 추가
- **CLI 및 API 지원**: 로컬에서 실행 가능

### ☁️ Cloud Version (Upcoming) | 클라우드 버전 (예정)
- **Notification System**: Sends review results via email, Slack, etc.
- **Automation of Repetitive Tasks**: Executes auto-refactoring based on defined criteria.
- **Enhanced Security Analysis**: Detects and recommends updates for library vulnerabilities.
- **Dashboard**: Provides project-specific code quality and review tracking.

- **알림 시스템**: 리뷰 결과를 이메일, 슬랙 등으로 전달
- **반복 작업 자동화**: 특정 기준 충족 시 자동 리팩토링 실행
- **보안 검사 강화**: 라이브러리 취약점 자동 탐지 및 업데이트 권장
- **대시보드 제공**: 프로젝트별 코드 품질 및 리뷰 내역 관리

## Installation & Execution | 설치 및 실행
### 1️⃣ Running Locally | 로컬에서 실행하기
```bash
git clone https://github.com/your-repo/code-review-ai.git
cd code-review-ai
pip install -r requirements.txt
python main.py
```

### 2️⃣ Running in GitHub Actions | GitHub Actions에서 실행
Add the following `.github/workflows/code-review.yml` file:
`.github/workflows/code-review.yml` 파일을 추가:
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

## How to Contribute | 참여 방법
### ✅ Contribution Guide | 기여 가이드
1. Check the issues and choose a task.
2. Create a `feature-branch` and start development.
3. Submit a PR for a code review request.
4. Once reviewed, the changes will be merged.

1. 이슈를 확인하고 원하는 작업을 선택하세요.
2. `feature-branch`를 생성하고 개발을 진행하세요.
3. PR을 생성하여 코드 리뷰 요청을 보내세요.
4. 코드 리뷰 후, 머지되면 반영됩니다.

### 🛠 Development Stack | 개발 환경
- **Backend**: FastAPI, Celery
- **AI Models**: GPT-4, Claude, Mistral
- **Database**: PostgreSQL, Redis
- **Deployment**: Docker, Kubernetes
- **Testing**: pytest, Jest

- **백엔드**: FastAPI, Celery
- **AI 모델**: GPT-4, Claude, Mistral
- **데이터베이스**: PostgreSQL, Redis
- **배포**: Docker, Kubernetes
- **테스트**: pytest, Jest

## Recruiting Contributors | 컨트리뷰터 모집
This project is open to all contributors. We are looking for help in the following roles:

이 프로젝트는 누구나 기여할 수 있으며, 아래와 같은 역할이 필요합니다.

### 🎯 Contributor Roles | 컨트리뷰터 역할
- **Core Developer**: AI model optimization, backend development, performance enhancements.
- **Frontend Developer**: Web dashboard and VS Code extension development.
- **Tester & QA**: Automated testing, code reviews.
- **Documentation Specialist**: Writing README, tutorials, API documentation.
- **Community Manager**: Managing issues, answering questions, improving contribution guidelines.
- **UI/UX Designer**: Improving usability and interface design.

- **코어 개발자**: AI 모델 최적화, 백엔드 개발, 성능 개선
- **프론트엔드 개발자**: 웹 대시보드 및 VS Code 확장 개발
- **테스터 및 품질 관리**: 테스트 자동화, 코드 검토
- **문서화 전문가**: README, 튜토리얼, API 문서 정리
- **커뮤니티 관리자**: 이슈 관리, 질문 응답, 기여 가이드 개선
- **UI/UX 디자이너**: 사용성 개선 및 인터페이스 디자인

**👉 How to Apply | 지원 방법:** Check out the "Manager Recruitment" issues labeled on our [GitHub Issues](https://github.com/your-repo/devbuddy/issues) page and apply!

**👉 지원 방법:** [GitHub Issues](https://github.com/your-repo/devbuddy/issues) 페이지에서 "Manager Recruitment" 라벨이 붙은 이슈를 확인하고 지원하세요!

---

### 🛠 **Competitor Services and Feature Comparison | 경쟁 서비스 및 기능 비교**

| Service Name | Launch Date | Open Source | GitHub Repository | Active Status | Key Features | Target Users | Distinguishing Features |
|--------------|-------------|-------------|-------------------|---------------|--------------|--------------|-------------------------|
| **DevBuddy** | 2025 | ✅ Yes | [DevBuddy GitHub](https://github.com/your-repo/devbuddy) | Active | AI code review, automated test generation, documentation, GitHub Actions support | Solo developers, startups | User-friendly UI, tailored for solo developers |
| **Codacy** | 2014 | ✅ Partial | [Codacy GitHub](https://github.com/codacy) | Active | Code analysis, security checks, test automation | Enterprises, teams | Focus on security and quality | citeturn0search6
| **DeepCode** | 2019 | ✅ Yes | [DeepCode GitHub](https://github.com/DeepCodeAI) | Integrated into Snyk | AI-based code review, static analysis | Developers, open-source projects | Machine learning-driven static analysis |
| **SonarQube** | 2007 | ✅ Yes | [SonarQube GitHub](https://github.com/SonarSource/sonarqube) | Active | Code quality and security analysis | Enterprises, large-scale projects | Comprehensive large-scale solution | citeturn0search4
| **GitHub Copilot** | 2021 | ❌ No | N/A | Active | AI code autocompletion, some code review capabilities | All developers | Real-time code autocompletion | citeturn0search1

🚀 DevBuddy aims to be an **AI code review service centered on solo developers**, maximizing developer productivity! We look forward to your interest and participation. 💡✨

🚀 DevBuddy는 **1인 개발자 중심의 AI 코드 리뷰 서비스**로, 개발자 생산성을 극대화하는 것을 목표로 합니다! 여러분의 관심과 참여를 기다립니다. 💡✨ 




---

## 📝 License | 라이선스

This project is licensed under the MIT License.이 프로젝트는 MIT 라이선스를 따릅니다.

🔹 What is MIT License?
The MIT License is a permissive open-source license that allows anyone to use, modify, and distribute the software with minimal restrictions.
It is widely used in open-source projects because it provides flexibility and encourages collaboration.
All you need to do is include the original license notice when redistributing the code.

🔹 MIT 라이선스란?
MIT 라이선스는 누구나 소프트웨어를 사용, 수정, 배포할 수 있도록 허용하는 자유로운 오픈소스 라이선스입니다.
이 라이선스는 사용자의 자유도를 높여 협업을 장려하며, 오픈소스 프로젝트에서 널리 사용됩니다.
배포 시 원본 라이선스 공지를 포함하면 자유롭게 활용할 수 있습니다.

## Community & Support | 커뮤니티 및 지원
- 💬 [Discord Channel](https://discord.gg/7bSqAjPZDe)
- 📧 Email: support@baryon.ai
- 📝 [Contribution Guide](CONTRIBUTING.md)

---
🚀 **Join us in building the AI-powered code review ecosystem!**
🚀 **함께 AI 기반 코드 리뷰 생태계를 만들어 가요!**
