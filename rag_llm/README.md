# RAG & LLM 학습 로그

##  학습 목표
- RAG(Retrieval-Augmented Generation) 시스템 구축 마스터
- 벡터 데이터베이스 활용한 효율적인 문서 검색 구현
- LLM과 RAG의 통합을 통한 실용적 애플리케이션 개발

##  기술 스택
- **LLM**: OpenAI GPT-4, Claude, Local LLM (Ollama)
- **Vector DB**: ChromaDB, Pinecone, Weaviate
- **Embedding**: OpenAI Embeddings, HuggingFace Sentence Transformers
- **Framework**: LangChain, LlamaIndex
- **Document Processing**: PyPDF2, Unstructured

##  학습 내용

### 1. RAG 시스템 기초
- [ ] RAG 아키텍처 이해 (Retrieval + Generation)
- [ ] 벡터 임베딩의 원리와 활용
- [ ] 유사도 검색 알고리즘
- [ ] 문서 청킹(Chunking) 전략

### 2. 문서 처리 및 임베딩
- [ ] 다양한 문서 형식 처리 (PDF, Word, HTML, Markdown)
- [ ] 텍스트 전처리 및 정규화
- [ ] 임베딩 모델 선택 및 최적화
- [ ] 메타데이터 관리

### 3. 벡터 데이터베이스
- [ ] ChromaDB 설치 및 설정
- [ ] 벡터 저장 및 검색 최적화
- [ ] 인덱싱 전략
- [ ] 확장성 고려사항

### 4. 검색 최적화
- [ ] 하이브리드 검색 (Dense + Sparse)
- [ ] 리랭킹(Re-ranking) 기법
- [ ] 쿼리 확장 및 개선
- [ ] 검색 결과 필터링

### 5. LLM 통합
- [ ] Prompt Engineering for RAG
- [ ] Context Window 관리
- [ ] 응답 품질 향상 기법
- [ ] Hallucination 방지 전략

### 6. 고급 RAG 패턴
- [ ] Multi-hop RAG (복수 단계 검색)
- [ ] Conversational RAG (대화형 검색)
- [ ] Adaptive RAG (적응형 검색)
- [ ] Graph RAG (지식 그래프 기반)

##  실습 프로젝트

### 1. 문서 기반 QA 시스템
- PDF 문서 업로드 및 자동 인덱싱
- 자연어 질문에 대한 정확한 답변 생성
- 답변 근거 문서 위치 제공

### 2. 기술 문서 도우미
- API 문서, 기술 매뉴얼 검색
- 코드 예제 및 설명 제공
- 버전별 문서 관리

### 3. 법률/규정 검색 시스템
- 복잡한 법률 문서에서 관련 조항 검색
- 판례 및 해석 제공
- 규정 변경사항 추적

### 4. 개인화된 학습 도우미
- 학습 자료 기반 맞춤형 설명
- 개념 간 연결고리 제공
- 학습 진도에 따른 내용 추천

##  학습 기록

### 이전 학습 내용 (Claude와의 대화 기록)
- RAG 시스템 아키텍처 설계 논의
- 벡터 데이터베이스 선택 기준 및 비교
- 문서 청킹 전략과 성능 최적화 방법
- LangChain을 활용한 RAG 파이프라인 구축
- 하이브리드 검색과 리랭킹 기법 학습
- 대화형 RAG 시스템 설계 고민

### 2025-09-10
- RAG 학습 체계 정리 및 실습 계획 수립
- 프로젝트별 우선순위 설정

### 다음 학습 계획
- ChromaDB를 사용한 첫 번째 RAG 시스템 구현
- 다양한 문서 형식 처리 실습
- 검색 품질 평가 및 개선

##  RAG 시스템 아키텍처

### 기본 RAG 파이프라인
```
문서 → 청킹 → 임베딩 → 벡터DB 저장
               ↓
사용자 질문 → 임베딩 → 유사도 검색 → 관련 문서
               ↓
       LLM (질문 + 문서) → 답변 생성
```

### 고급 RAG 패턴
- **Query Enhancement**: 질문 재작성 및 확장
- **Multi-step Retrieval**: 단계별 정보 수집
- **Self-reflection**: 답변 검증 및 개선

##  성능 측정 지표
- **검색 정확도**: Precision@K, Recall@K
- **답변 품질**: BLEU, ROUGE, BERTScore
- **응답 속도**: 검색 시간, 생성 시간
- **사용자 만족도**: 피드백 점수

##  참고 자료
- [LangChain RAG 문서](https://python.langchain.com/docs/use_cases/question_answering/)
- [LlamaIndex 문서](https://docs.llamaindex.ai/)
- [ChromaDB 문서](https://docs.trychroma.com/)
- [RAG 관련 논문](https://arxiv.org/abs/2005.11401)
