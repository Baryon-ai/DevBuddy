# 🚀 **DevBuddy: AI Code Review Service (Open Source)** 
> DevBuddy: AI 코드 리뷰 서비스 (오픈소스)

| **[Korean](README.md)** | **[English](README_ENG.md)** |

---

## 🎯 **Introduction | 소개**
🤖 **DevBuddy**는 1인 개발자를 위한 **AI 기반 자동 코드 리뷰 서비스**입니다.  
코드를 푸시할 때마다 자동으로 리뷰하고, 개선 사항을 제안하며, **단위 테스트를 생성**해 개발자가 창의적인 작업에 집중할 수 있도록 돕습니다! 🎨✨

🚀 **초기 버전은 오픈소스로 제공**되며, **클라우드 버전**에서는 추가 기능(알림, 반복 작업 자동화, 보안 강화 등)이 제공될 예정입니다.

---

## 🔍 **예시 프로젝트: Hello-MCP**

DevBuddy의 기능을 직접 체험해볼 수 있는 **[Hello-MCP](https://github.com/hongsw/hello-mcp)** 예시 프로젝트를 준비했습니다. 이 저장소는 DevBuddy의 코드 리뷰 및 개선 제안 기능을 테스트할 수 있도록 다양한 코드 패턴과 개선 가능한 요소들을 포함하고 있습니다.

- **커밋 및 PR 히스토리**: 실제 개발 워크플로우를 시뮬레이션한 다양한 커밋과 PR 예시
- **의도적인 코드 이슈**: AI가 식별하고 개선할 수 있는 다양한 코드 문제점 포함
- **간단한 활용 방법**: 저장소를 클론하여 DevBuddy 연동 후 자동 코드 리뷰 체험 가능

이 예시 프로젝트를 통해 DevBuddy가 어떻게 코드 품질을 개선하고 개발자의 생산성을 높이는지 직접 확인해보세요!

---

## 🛠 **Features | 기능**

### 📌 **Core Features (Open Source) | 기본 기능 (오픈소스)**
- **자동 코드 리뷰**:  
  AI가 코드 스타일, 버그 가능성, 보안 취약점을 분석합니다.
- **개선 아이디어 제공**:  
  성능 최적화와 리팩토링을 제안합니다.
- **자동 단위 테스트 생성**:  
  AI가 함수 분석 후 테스트 코드를 작성합니다.
- **코드 설명 및 문서화**:  
  자동으로 문서를 생성하고 설명합니다.
- **Git 연동**:  
  GitHub/GitLab에서 **PR 자동 리뷰 및 코멘트**를 추가합니다.
- **CLI 및 API 지원**:  
  로컬에서도 실행 가능합니다.

---

### ☁️ **Cloud Version (Upcoming) | 클라우드 버전 (예정)**
- **알림 시스템**:  
  리뷰 결과를 **이메일, 슬랙** 등으로 전달합니다.
- **반복 작업 자동화**:  
  특정 기준에 따라 **자동 리팩토링**을 실행합니다.
- **보안 검사 강화**:  
  라이브러리 취약점을 탐지하고 **업데이트를 권장**합니다.
- **대시보드 제공**:  
  프로젝트별 **코드 품질** 및 **리뷰 내역**을 관리합니다.

---

## 🚀 **Installation & Execution | 설치 및 실행**

### 1️⃣ **로컬에서 실행하기**
```bash
git clone https://github.com/your-repo/code-review-ai.git
cd code-review-ai
pip install -r requirements.txt
python main.py
```

---

### 2️⃣ **GitHub Actions에서 실행**
`.github/workflows/code-review.yml` 파일 추가:
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

## ✅ **How to Contribute | 기여 방법**
1. **이슈 확인:** 작업을 선택하세요.  
2. **브랜치 생성:** `feature-branch`를 만들어 개발을 시작하세요.  
3. **PR 생성:** 코드 리뷰 요청을 보내세요.  
4. **머지:** 리뷰 후 반영됩니다.

### 🛠 **Development Stack | 개발 환경**
- **Backend**: FastAPI, Celery  
- **AI Models**: GPT-4, Claude, Mistral  
- **Database**: PostgreSQL, Redis  
- **Deployment**: Docker, Kubernetes  
- **Testing**: pytest, Jest  

### 🎯 **Contributor Roles | 컨트리뷰터 역할**
- **코어 개발자**: AI 모델 최적화, 백엔드 개발, 성능 개선
- **프론트엔드 개발자**: 웹 대시보드 및 VS Code 확장 개발
- **테스터 및 품질 관리**: 테스트 자동화, 코드 검토
- **문서화 전문가**: README, 튜토리얼, API 문서 정리
- **커뮤니티 관리자**: 이슈 관리, 질문 응답, 기여 가이드 개선
- **UI/UX 디자이너**: 사용성 개선 및 인터페이스 디자인

<br>

👉 **지원 방법:** [GitHub Issues](https://github.com/your-repo/devbuddy/issues)에서 "Manager Recruitment" 라벨을 확인하세요!

---

## 🛠 **Competitor Services and Feature Comparison | 경쟁 서비스 및 기능 비교**

| Service Name | Launch Date | Open Source | GitHub Repository | Active Status | Key Features | Target Users | Distinguishing Features |
|--------------|-------------|-------------|-------------------|---------------|--------------|--------------|-------------------------|
| **DevBuddy** | 2025 | ✅ Yes | [DevBuddy GitHub](https://github.com/your-repo/devbuddy) | Active | AI code review, automated test generation, documentation, GitHub Actions support | Solo developers, startups | User-friendly UI, tailored for solo developers |
| **Codacy** | 2014 | ✅ Partial | [Codacy GitHub](https://github.com/codacy) | Active | Code analysis, security checks, test automation | Enterprises, teams | Focus on security and quality | citeturn0search6
| **DeepCode** | 2019 | ✅ Yes | [DeepCode GitHub](https://github.com/DeepCodeAI) | Integrated into Snyk | AI-based code review, static analysis | Developers, open-source projects | Machine learning-driven static analysis |
| **SonarQube** | 2007 | ✅ Yes | [SonarQube GitHub](https://github.com/SonarSource/sonarqube) | Active | Code quality and security analysis | Enterprises, large-scale projects | Comprehensive large-scale solution | citeturn0search4
| **GitHub Copilot** | 2021 | ❌ No | N/A | Active | AI code autocompletion, some code review capabilities | All developers | Real-time code autocompletion | citeturn0search1

🚀 DevBuddy는 **1인 개발자 중심의 AI 코드 리뷰 서비스**로, 개발자 생산성을 극대화하는 것을 목표로 합니다! 여러분의 관심과 참여를 기다립니다. 💡✨ 

---

## 📝 **License | 라이선스**
이 프로젝트는 **MIT 라이선스**를 따릅니다.  

🔹 **MIT 라이선스란?**
> MIT 라이선스는 누구나 소프트웨어를 사용, 수정, 배포할 수 있도록 허용하는 자유로운 오픈소스 라이선스입니다. 이 라이선스는 사용자의 자유도를 높여 협업을 장려하며, 오픈소스 프로젝트에서 널리 사용됩니다. 배포 시 원본 라이선스 공지를 포함하면 자유롭게 활용할 수 있습니다.

---

## Community & Support | 커뮤니티 및 지원
- 💬 [Discord Channel](https://discord.gg/7bSqAjPZDe)
- 📧 Email: support@baryon.ai
- 📝 [Contribution Guide](CONTRIBUTING.md)

---
🚀 **함께 AI 기반 코드 리뷰 생태계를 만들어 가요!**
