# GOPIZZA Task Management System (Govis Task)

![대쉬보드 이미지](https://github.com/futureplanning/front-rnd/blob/master/public/dash_boadrd2.png?raw=true)

![작업,일정 이미지](https://raw.githubusercontent.com/futureplanning/front-rnd/refs/heads/master/public/tasks_list.png)

![평가 및 성과관리 이미지](https://raw.githubusercontent.com/futureplanning/front-rnd/refs/heads/master/public/evalution.png)

![Report 이미지](https://raw.githubusercontent.com/futureplanning/front-rnd/refs/heads/master/public/report.png)

![LLM](https://raw.githubusercontent.com/futureplanning/front-rnd/refs/heads/master/public/llm.png)


## 프로젝트 개요

Govis Task는 고피자의 혁신적인 업무 관리 시스템으로, 조직 내 업무의 복잡성을 효율적으로 관리하기 위해 개발된 스마트 워크 플랫폼입니다. 직급과 권한에 따라 차별화된 인사이트를 제공하여 모든 구성원이 최적의 의사결정을 할 수 있도록 지원합니다. 실시간 업무 진행 상황 모니터링, 투명한 성과 관리, 데이터 기반 의사결정을 통해 조직의 업무 문화를 혁신합니다.

## 주요 특징

### 1. 직급별 맞춤형 대시보드

- **일반 직원**: 자신의 현재 작업 현황, 개인 성과 지표, 마감일 임박 작업 알림
- **팀장**: 팀 전체 작업 진행 상황, 팀원별 업무 부하 및 성과 분석, 리소스 최적화
- **본부장/이사**: 조직 전체 성과 메트릭스, 부서간 협업 현황, 전략적 의사결정 데이터

### 2. 스마트한 작업 및 일정 관리

- 진행 상태별 작업 분류 (예정/진행중/검토/완료/보류)
- 실시간 작업 시간 기록 및 분석
- 다양한 캘린더 뷰 (월간/주간/일간)
- 리소스 충돌 방지 및 적정 작업량 유지

### 3. 객관적인 평가 및 성과 관리

- 체계적인 평가 기준 (난이도, 성과 점수, 상세 피드백)
- 직급별 평가 권한 관리
- 다차원 성과 분석 및 맞춤형 성과 리포트
- 투명한 피드백 시스템

### 4. 데이터 기반 리포트 시스템

- 개인, 팀, 경영진을 위한 맞춤형 리포트
- 실시간 데이터 업데이트 및 모바일 최적화
- 다차원 데이터 분석 및 패턴 분석
- 주간/월간 리포트 자동 생성

### 5. AI 기반 데이터 분석

- 자연어 기반 데이터 조회 및 질의응답
- 실시간 SQL 쿼리 자동 생성
- 인력 현황, 성과, 업무 효율성 분석
- 지속적 학습 및 개선

## 기술 스택

### 프론트엔드
- **프레임워크**: Next.js 15
- **라이브러리**: React 19 (RC)
- **언어**: TypeScript
- **상태 관리**: MobX
- **데이터 페칭**: TanStack Query (React Query)
- **UI 컴포넌트**: Material UI 6
- **스타일링**: Emotion
- **폼 관리**: React Hook Form, Yup
- **차트**: Recharts
- **애니메이션**: Framer Motion
- **알림**: React Toastify
- **HTTP 클라이언트**: Axios



## 프로젝트 구조

```
GovisTaskFront/
├── public/               # 정적 파일
│   └── images/           # 이미지 리소스
├── src/                  # 소스 코드
│   ├── components/       # 재사용 컴포넌트
│   ├── lib/              # 유틸리티 함수 및 서비스
│   ├── pages/            # 페이지 컴포넌트
│   ├── stores/           # MobX 스토어
│   ├── styles/           # 전역 스타일
│   └── types/            # TypeScript 타입 정의
├── next.config.ts        # Next.js 설정
└── tsconfig.json         # TypeScript 설정
```

## 설치 및 실행 방법

### 개발 환경 요구사항
- Node.js 18.0 이상
- Yarn 또는 npm 패키지 매니저

### 설치 및 실행

```bash
# 1. 프로젝트 클론
git clone https://github.com/gopizza/GovisTask.git
cd GovisTaskFront

# 2. 의존성 설치
yarn install

# 3. 개발 서버 실행
yarn dev

# 4. 프로덕션 빌드
yarn build

# 5. 프로덕션 서버 실행
yarn start
```

개발 서버는 기본적으로 [http://localhost:3000](http://localhost:3000)에서 실행됩니다.

## 핵심 구현 특징

### 1. 반응형 대시보드
작업 현황과 성과 지표를 시각적으로 표현하는 대시보드는 다양한 디바이스와 화면 크기에 최적화되어 있으며, 사용자의 역할과 권한에 따라 맞춤형 정보를 제공합니다.

### 2. 실시간 작업 관리
Tanstack Query를 활용한 효율적인 데이터 페칭과 캐싱으로 실시간 업데이트를 구현하여, 항상 최신 정보를 기반으로 의사결정을 할 수 있습니다.

### 3. 직관적인 캘린더 인터페이스
사용자가 쉽게 일정을 관리하고 시각화할 수 있는 직관적인 인터페이스를 제공합니다.

### 4. 데이터 시각화
Recharts를 활용한 다양한 차트와 그래프로 복잡한 데이터를 직관적으로 이해할 수 있도록 시각화했습니다.

### 5. 유연한 권한 관리
사용자의 역할과 직급에 따라 자동으로 기능과 뷰를 조정하는 권한 관리 시스템을 구현하여, 정보의 접근성과 보안을 동시에 확보했습니다.

## 비즈니스 가치

1. **업무 효율성 향상**: 작업 진행 상황 실시간 파악, 리소스 배분 최적화, 불필요한 회의/보고 감소
2. **투명한 성과 관리**: 객관적인 평가 지표 확보, 공정한 보상 체계 구축, 성과 데이터 자동 집계
3. **조직 문화 혁신**: 수평적 소통 문화 정착, 데이터 기반 의사결정, 자율적인 업무 환경 조성
4. **리스크 관리 강화**: 지연 작업 조기 발견, 병목 구간 식별, 선제적 대응 가능

