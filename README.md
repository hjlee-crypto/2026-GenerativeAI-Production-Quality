# 생성형 AI를 활용한 생산·품질 데이터 분석 및 시각화

**Generative AI for Production and Quality Data Analysis & Visualization**

**성결대학교 산업경영공학과 4학년 특강**

- **강의:** 이현주 교수 | 한성대학교 AI응용학과
- **교육 시간:** 90분
- **실습 도구:** Google Colab, Google Gemini, Julius AI

---

## 1. 특강 소개

본 특강은 제조 현장의 생산·품질 데이터를 생성형 AI로 분석하고 시각화하여, 생산관리 및 품질관리 업무에 필요한 문제 해결 역량을 기르는 실습 중심 프로그램입니다.

학생들은 가상의 제조기업 데이터를 활용하여 생산 실적과 불량률을 분석하고, 분석 결과를 바탕으로 현장 개선 방안을 도출합니다.

### 학습 목표

1. 생산·품질관리 업무에서 생성형 AI의 활용 방법 이해
2. 생산계획 달성률, 불량률 등 주요 관리 지표 분석
3. 생산 실적 비교 차트 및 불량 유형 파레토 차트 작성
4. AI 분석 결과 검증 및 생산·품질 개선 방안 도출

## 2. 실습자료 구성

```text
2026-GenerativeAI-Production-Quality/
├── README.md
├── data/
│   ├── production_daily.csv
│   └── defect_types.csv
├── docs/
│   ├── PROMPTS.md
│   ├── JULIUS_AI_PRACTICE.md
│   ├── INSTRUCTOR_GUIDE.md
│   ├── STUDENT_WORKSHEET_DRIVE_GITHUB.md
│   ├── WHY_THIS_PRACTICE.md
│   └── WORKSHEET.md
└── notebooks/
    ├── production_quality_workshop_DRIVE.ipynb
    └── production_quality_workshop.ipynb
```

### 주요 파일 안내

| 구분 | 파일 | 내용 |
|---|---|---|
| 생산 데이터 | `production_daily.csv` | 생산계획 및 실적 분석 |
| 품질 데이터 | `defect_types.csv` | 불량 유형 및 파레토 분석 |
| 실습 노트북 | `production_quality_workshop_DRIVE.ipynb` | Google Drive 연동 실습 |
| 실습 노트북 | `production_quality_workshop.ipynb` | 일반 Colab 실습 |
| AI 활용 | `PROMPTS.md` | 생성형 AI 분석 프롬프트 |
| AI 활용 | `JULIUS_AI_PRACTICE.md` | Julius AI 실습 안내 |
| 실습 안내 | `STUDENT_WORKSHEET_DRIVE_GITHUB.md` | Google Drive 및 GitHub 활용 안내 |
| 실습 안내 | `WORKSHEET.md` | 생산·품질 분석 실습 활동 |
| 실습 안내 | `WHY_THIS_PRACTICE.md` | 실습 목적 및 업무 활용 |
| 운영 자료 | `INSTRUCTOR_GUIDE.md` | 교수자용 실습 운영 안내 |

## 3. 실습자료 다운로드

1. GitHub 저장소 상단의 **Code** 버튼을 클릭합니다.
2. **Download ZIP**을 선택합니다.
3. 다운로드한 ZIP 파일의 압축을 해제합니다.
4. `data`, `docs`, `notebooks` 폴더를 확인합니다.

GitHub 계정이 없어도 공개 저장소의 자료를 다운로드할 수 있습니다.

## 4. Google Colab 실습 준비

### ① 본인 Google Drive에 자료 저장

Google Drive에 `production_quality_ai_workshop` 폴더를 생성하고 다음과 같이 실습자료를 업로드합니다.

```text
내 드라이브/
└── production_quality_ai_workshop/
    ├── data/
    │   ├── production_daily.csv
    │   └── defect_types.csv
    └── notebooks/
        ├── production_quality_workshop_DRIVE.ipynb
        └── production_quality_workshop.ipynb
```

### ② Google Colab 실행

1. [Google Drive](https://drive.google.com/)에 로그인합니다.
2. `notebooks` 폴더에서 `production_quality_workshop_DRIVE.ipynb` 파일을 찾습니다.
3. 파일을 마우스 오른쪽 버튼으로 클릭하고 **연결 앱 → Google Colaboratory**를 선택합니다.
4. 노트북을 열고 코드 셀을 순서대로 실행합니다.
5. Google Drive 접근 권한이 요청되면 승인합니다.

Google Colaboratory가 보이지 않는 경우 **연결 앱 → 앱 더 연결하기**에서 검색하여 연결합니다.

## 5. 실습 과제

### 실습 ① 생산관리 데이터 분석

**목적:** 생산계획 대비 실적을 분석하여 생산 차질이 발생한 생산라인을 파악합니다.

- 생산라인별 계획 생산량과 실제 생산량 비교
- 생산계획 달성률 계산
- 시간당 생산량 비교
- 생산 실적 비교 차트 작성

**확인할 사항:** 생산계획 달성률이 가장 낮은 라인은 어디이며, 어떤 추가 데이터가 필요할까요?

### 실습 ② 품질관리 데이터 분석

**목적:** 불량 데이터를 분석하여 품질 개선이 필요한 생산라인과 주요 불량 유형을 파악합니다.

- 생산라인별 불량률 계산
- 불량 유형별 발생 건수 분석
- 파레토 차트 작성
- 주요 불량 유형과 개선 우선순위 확인

**확인할 사항:** 어떤 불량 유형을 우선적으로 관리해야 하며, 그 이유는 무엇일까요?

### 실습 ③ 생성형 AI를 활용한 분석

[Julius AI](https://julius.ai/) 또는 [Google Gemini](https://gemini.google.com/)를 활용하여 생산·품질 데이터를 분석합니다.

**프롬프트 예시**

> 제공한 생산·품질 데이터를 분석해 주세요. 생산라인별 생산계획 달성률과 불량률을 계산하고 비교 차트를 작성해 주세요. 문제가 있는 생산라인을 데이터에 근거하여 설명하고, 추가로 확인해야 할 사항을 제시해 주세요. 데이터만으로 확인할 수 없는 원인은 추정으로 구분해 주세요.

AI가 제시한 계산 결과와 Colab 분석 결과를 비교하고 차이가 있다면 원인을 확인합니다.

### 실습 ④ 생산·품질 개선 방안 도출

앞선 분석 결과를 바탕으로 다음 항목을 정리합니다.

1. 주요 생산·품질 문제
2. 데이터 분석 결과 및 근거
3. 가능한 원인 가설
4. 개선 방안 및 우선순위
5. 추가로 확인해야 할 데이터

## 6. 최종 결과물 및 제출

### 최종 결과물

- 실행 결과가 포함된 Colab 노트북(`.ipynb`)
- 생산계획 대비 실적 비교 차트
- 불량 유형 파레토 차트
- 생산·품질 개선 방안 요약

### 방법 ① Google Drive 링크 공유

1. 본인 Google Drive에 완성한 Colab 노트북을 저장합니다.
2. 공유 설정에서 링크가 있는 사용자의 열람 권한을 설정합니다.
3. 교수자가 안내한 제출 경로로 링크를 전달합니다.

### 방법 ② 본인 GitHub에 업로드 (선택)

1. 본인 GitHub 저장소를 생성하거나 이 저장소를 Fork합니다.
2. 완성한 Colab 노트북, 차트, 분석 결과를 업로드합니다.
3. 교수자가 안내한 제출 경로로 저장소 링크를 전달합니다.

GitHub 계정이 없는 학생은 Google Drive 링크로 결과물을 공유할 수 있습니다.

## 7. 실습 시 유의사항

- 실습 데이터는 교육용 가상 데이터입니다.
- 생성형 AI의 계산 결과는 원본 데이터와 비교하여 검증합니다.
- 데이터에서 관찰된 현상과 추정한 원인을 구분합니다.
- 실제 기업의 기밀자료나 개인정보를 공개형 AI 서비스에 업로드하지 않습니다.
- 무료 AI 서비스의 사용량 제한이 발생하면 Google Colab을 활용합니다.

---

**성결대학교 산업경영공학과 | 생성형 AI 생산·품질 데이터 분석 특강**

이현주 교수 · 한성대학교 AI응용학과
