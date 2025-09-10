# Backend 개발 기록

##  사용 기술 스택
- **Framework**: Spring Boot
- **Database**: MariaDB
- **언어**: Java
- **형상관리**: Git (GitHub)

## 백앤드 디렉토리(보안상 실제와 상이함)
```
ProjectRoot/                           # 프로젝트 루트
│  README.md                           # 프로젝트 도움말 / 안내 문서
│  build.sh                            # 빌드 실행 스크립트 (Linux/Mac)
│  build.cmd                           # 빌드 실행 스크립트 (Windows)
│  project.xml                         # 프로젝트 설정 파일 (ex: pom.xml)
│  structure.txt                       # 디렉토리 구조 출력본
│
├─src/                                 # 소스 코드 루트
│  ├─main/                             # 메인 소스 디렉토리
│  │  ├─java/                          # 자바 코드
│  │  │  └─com/company/app/            # 패키지 루트
│  │  │      │  module.iml             # IntelliJ 모듈 파일
│  │  │      │  MainApplication.java   # Spring Boot 시작점
│  │  │      │
│  │  │      ├─auth/                   # 인증(Authentication) 모듈
│  │  │      │  ├─dto/                 # 인증 요청/응답 DTO
│  │  │      │  │      UserDto.java
│  │  │      │  │      PasswordResetConfirmDto.java
│  │  │      │  │      PasswordResetRequestDto.java
│  │  │      │  │      TokenResponseDto.java
│  │  │      │  │      LoginRequestDto.java
│  │  │      │  │      RegisterRequestDto.java
│  │  │      │  ├─controller/          # 인증 API 컨트롤러
│  │  │      │  │      AuthController.java
│  │  │      │  ├─service/             # 인증 서비스
│  │  │      │  │      TokenService.java
│  │  │      │  │      AuthService.java
│  │  │      │  │      MailService.java
│  │  │      │  ├─security/            # 보안/인증 관련
│  │  │      │  │      TokenProvider.java
│  │  │      │  │      TokenFilter.java
│  │  │      │  │      SecurityConfig.java
│  │  │      │  │      UserDetailsServiceImpl.java
│  │  │      │  ├─entity/              # 인증 엔티티
│  │  │      │  │      SignupRequestEntity.java
│  │  │      │  │      UserEntity.java
│  │  │      │  │      ResetTokenEntity.java
│  │  │      │  └─repository/          # 인증 Repository
│  │  │      │          ResetTokenRepository.java
│  │  │      │          SignupRequestRepository.java
│  │  │      │          UserRepository.java
│  │  │      │
│  │  │      ├─profile/                # 마이페이지(사용자 프로필) 기능
│  │  │      │  ├─dto/
│  │  │      │  ├─controller/          # 프로필 API 컨트롤러
│  │  │      │  │      ProfileController.java
│  │  │      │  ├─service/             # 프로필 서비스
│  │  │      │  │      ProfileService.java
│  │  │      │  ├─entity/
│  │  │      │  └─repository/
│  │  │      │
│  │  │      ├─agent/                  # AI 에이전트 모듈
│  │  │      │  ├─dto/
│  │  │      │  ├─controller/          # 에이전트 API 컨트롤러
│  │  │      │  │      AgentController.java
│  │  │      │  ├─service/             # 에이전트 서비스
│  │  │      │  │      AgentService.java
│  │  │      │  ├─entity/
│  │  │      │  ├─config/              # 에이전트 관련 설정
│  │  │      │  │      WebConfig.java
│  │  │      │  └─repository/
│  │  │      │
│  │  │      ├─chat/                   # 채팅 모듈
│  │  │      │  ├─dto/
│  │  │      │  │  ├─response/         # 채팅 응답 DTO
│  │  │      │  │  │      ConversationListDto.java
│  │  │      │  │  │      MessageDto.java
│  │  │      │  │  │      MessageListDto.java
│  │  │      │  │  │      ConversationDto.java
│  │  │      │  │  └─request/          # 채팅 요청 DTO
│  │  │      │  │          SendMessageDto.java
│  │  │      │  │          CreateConversationDto.java
│  │  │      │  │          UpdateConversationDto.java
│  │  │      │  ├─controller/          # 채팅 API 컨트롤러
│  │  │      │  │      MessageController.java
│  │  │      │  │      ConversationController.java
│  │  │      │  ├─service/             # 채팅 서비스
│  │  │      │  │      ConversationService.java
│  │  │      │  │      MessageService.java
│  │  │      │  │      AIService.java
│  │  │      │  ├─entity/              # 채팅 엔티티
│  │  │      │  │      ConversationEntity.java
│  │  │      │  │      MessageEntity.java
│  │  │      │  │      MessageTyp
```


##  개발 진행 기록

### 1단계: 프로젝트 초기 설정
- [] **DB 설계**: 에이전트 챗봇 시스템용 데이터베이스 스키마 설계
- [] **MariaDB 연동**: Spring Boot 프로젝트와 MariaDB 연결 설정
- [] **연결 테스트**: 데이터베이스 연동 정상 동작 확인
- [] **GitHub 설정**: dev 브랜치 생성 및 README.md 마크다운 포맷 작성

### 2단계: 회원 관리 시스템
- [] **로그인 구현**: 사용자 인증 시스템 개발
- [] **회원가입 구현**: 신규 사용자 등록 기능 개발
- [] **입력값 검증**: 공백 입력 시 오류 처리 로직 추가
- [] **HTTP 상태 코드**: 적절한 응답 코드 반환 처리
- [] **마이페이지**: 사용자 정보 조회 및 관리 페이지 구현

### 3단계: 프론트엔드 연동
- [] **API 개발**: 회원가입/로그인 기능의 프론트엔드 연동 API 개발
- [] **CORS 설정**: 프론트엔드와의 원활한 통신을 위한 설정

### 4단계: 채팅 시스템 고도화
- [] **채팅방 설계**: 단순 구조에서 체계적 구조로 개선
  - 채팅방 ID, 메시지 ID, 사용자 ID 분리 관리
  - 향후 확장성을 고려한 데이터베이스 구조 설계
- [] **관리자 권한**: admin 페이지 접근 제어 기능 구현
  - 세분화된 접근 권한 관리
  - 보안성 강화

### 5단계: 보안 및 사용자 편의성 개선
- [] **비밀번호 찾기**: 전체 프로세스 신규 구현
  - 이메일 발송 → 인증코드 검증 → 비밀번호 재설정
  - 사용자 편의성 및 보안 강화
- [] **코드 품질**: 전체 코드 주석 추가 및 중간 점검
  - 오류 및 개선 포인트 조기 확인
  - 개발 안정성 제고

### 6단계: AI Agent 연동
- [] **AI Agent 통합**: 백엔드에 AI Agent 코드 및 보안 처리 로직 추가
- [] **연동 테스트**: AI Agent ↔ 백엔드 연동 및 정상 동작 테스트 완료
- [] **구조 정리**: 추후 기능 확장을 위한 기반 코드 구조 정리
- [] **챗봇 로직 분석**: 향후 지능형 기능 확장 가능성 검토

##  데이터베이스 설계

### 채팅 시스템 테이블 구조
```sql
-- 사용자 테이블
users (user_id, username, email, password, created_at)

-- 채팅방 테이블  
chat_rooms (room_id, room_name, created_by, created_at)

-- 메시지 테이블
messages (message_id, room_id, user_id, content, timestamp)

-- 관리자 권한 테이블
admin_permissions (user_id, permission_level, granted_at)
```

##  보안 구현사항

### 인증 및 권한 관리
- JWT 토큰 기반 인증 시스템
- 관리자 페이지 접근 제어
- 비밀번호 암호화 저장

### 입력값 검증
- 회원가입 시 필수 필드 검증
- SQL Injection 방지
- XSS 공격 방지

##  성과 및 배운 점

### 기술적 성과
1. **확장 가능한 아키텍처**: 채팅방 시스템을 ID 분리 구조로 설계하여 향후 확장성 확보
2. **보안 강화**: 다층 보안 구조 구현으로 시스템 안정성 향상
3. **사용자 경험**: 비밀번호 찾기 등 편의 기능으로 UX 개선

### 협업 경험
- 민근홍 주임과의 서버 이전 작업 협업
- Git 브랜치 전략을 통한 체계적 형상관리
- 프론트엔드 팀과의 API 연동 경험

##  서버 이전 작업 경험

### 에스티리서치 홈페이지 이전
- [] **기존 호스팅 제거**: 기존 서버 삭제 작업 완료
- [] **신규 호스팅 개설**: 새로운 서버 환경 구축
- [] **리다이렉트 설정**: 에스티리서치 → 이노베이션 홈페이지 자동 이동 구현

##  다음 개발 계획
- AI Agent 성능 최적화
- 실시간 채팅 기능 고도화  
- 모니터링 및 로깅 시스템 구축
- API 문서화 자동화


