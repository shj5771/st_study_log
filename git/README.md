# Git 사용 기록

##  프로젝트 형상관리 경험
실무 프로젝트에서의 Git 활용 및 협업 경험 기록

## 🛠 사용 환경
- **플랫폼**: GitHub
- **도구**: Git CLI, VS Code Git 확장
- **협업**: 팀 프로젝트 브랜치 전략

##  실제 사용 기록

### 프로젝트 초기 설정
- [] **저장소 생성**: 에이전트 챗봇 시스템 GitHub 저장소 생성
- [] **브랜치 전략**: dev 브랜치 생성 및 개발 환경 분리
- [] **README 작성**: 마크다운 포맷으로 프로젝트 문서화
- [] **초기 커밋**: 프로젝트 구조 및 기본 설정 파일 커밋

### 개발 워크플로우 적용
```bash
# 개발 브랜치 생성 및 전환
git checkout -b dev
git push -u origin dev

# 기능 개발 후 커밋
git add .
git commit -m "feat: 회원가입 기능 구현 및 입력값 검증 추가"
git push origin dev

# README.md 업데이트
git add README.md
git commit -m "docs: 프로젝트 구조 및 기능 설명 추가"
git push origin dev
```

### 실제 커밋 히스토리
- [x] **Initial commit**: 프로젝트 초기 구조 설정
- [x] **feat: DB 설계서 주임과 협업
- **역할**: 기존 서버 삭제 및 신규 서버 구축
- **Git 활용**: 
  - 작업 전 브랜치 생성 및 백업
  - 작업 단계별 커밋으로 진행 상황 추적
  - 작업 완료 후 문서화 및 커밋

### 프론트엔드 팀과의 API 연동
- **API 문서화**: README에 API 스펙 명시
- **버전 관리**: API 변경 사항을 커밋 메시지로 명확히 표기
- **테스트 환경**: dev 브랜치를 통한 안정적인 테스트 환경 제공

##  Git 사용 통계 및 성과

### 커밋 활동
- **총 커밋 수**: 50+ 개
- **평균 커밋 주기**: 일 2-3회
- **코드 리뷰**: 주요 기능별 동료 리뷰 진행
- **문서화**: 모든 기능에 대한 README 업데이트

### 브랜치 관리 성과
- **충돌 발생**: 0건 (체계적 브랜치 전략으로 충돌 방지)
- **롤백 횟수**: 2회 (빠른 문제 발견 및 대응)
- **배포 안정성**: dev 브랜치 검증을 통한 안정적 배포

##  실제 사용한 Git 명령어

### 일상적 워크플로우
```bash
# 작업 시작
git heckout dev
git pull origin dev
git checkout -b feature/new-feature

# 개발 진행
git add .
git commit -m "feat: 새로운 기능 구현"
git push origin feature/new-feature

# 개발 완료 후 병합
git checkout dev
git merge feature/new-feature
git push origin dev
git branch -d feature/new-feature
```

### 문제 해결 경험
```bash
# 잘못된 커밋 수정
git commit --amend -m "수정된 커밋 메시지"

# 특정 파일만 스테이징
git add src/main/java/service/UserService.java
git commit -m "fix: 사용자 서비스 버그 수정"

# 작업 임시 저장
git stash
git checkout main
git stash pop
```

## 📚 학습한 Git 고급 기능

### 실제 활용한 기능
- **git stash**: 임시 작업 저장 및 브랜치 전환
- **git cherry-pick**: 특정 커밋만 선별적으로 적용
- **git rebase**: 커밋 히스토리 정리 및 선형화
- **git blame**: 코드 변경 이력 추적
- **git log --oneline**: 간단한 커밋 히스토리 확인

### 문제 해결 경험
1. **대용량 파일 처리**: .gitignore로 불필요한 파일 제외
2. **커밋 히스토리 정리**: interactive rebase로 커밋 메시지 수정
3. **브랜치 정책**: 기능별 브랜치로 작업 분리 및 관리

## 🎯 향후 개선 계획

### Git 워크플로우 고도화
- [ ] **Git Flow**: 더 체계적인 브랜치 전략 도입
- [ ] **Pre-commit Hook**: 코드 품질 검사 자동화
- [ ] **자동 배포**: GitHub Actions를 활용한 CI/CD 구축
- [ ] **코드 리뷰**: Pull Request 기반 코드 리뷰 프로세스

### 팀 협업 강화
- [ ] **브랜치 보호**: main/dev 브랜치 보호 규칙 설정
- [ ] **이슈 트래킹**: GitHub Issues와 커밋 연동
- [ ] **릴리즈 노트**: 자동 릴리즈 노트 생성
- [ ] **백업 전략**: 원격 저장소 다중화

## 📖 참고한 자료 및 학습
- [Git 공식 문서](https://git-scm.com/doc)
- [GitHub 협업 가이드](https://guides.github.com/)
- 팀 내 Git 워크플로우 가이드라인
- 실무 프로젝트를 통한 실전 경험
