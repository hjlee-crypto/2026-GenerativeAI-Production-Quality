# 생성형 AI 기반 생산·품질 데이터 분석 및 시각화 실습

**대상:** 산업경영공학과 4학년 · **시간:** 80분 · **도구:** Google Gemini(무료) + Google Colab(무료)

## 학습 목표
1. 생산계획 달성률, 불량률, 시간당 생산량, 시간가동률을 정확히 계산한다.
2. 생산라인별 지표와 불량 유형 파레토 차트를 시각화한다.
3. 생성형 AI의 분석 코드와 해석을 검증하고, 원인 **가설**과 추가 확인 데이터를 구분한다.
4. 분석 결과를 근거로 현장 개선 제안 1건을 작성한다.

## 실습 시작 (학생)
1. Google 계정으로 [Google Colab](https://colab.research.google.com/)에 로그인합니다.
2. GitHub에서 `notebooks/production_quality_workshop.ipynb`를 열고 **Open in Colab**을 선택하거나, Colab의 **파일 > 노트 업로드**로 해당 파일을 엽니다.
3. 노트북의 **첫 번째 코드 셀**에서 `DATA_BASE`를 GitHub 저장소의 Raw URL로 수정합니다. 예: `https://raw.githubusercontent.com/OWNER/REPO/main/data/` (끝의 `/` 포함). 저장소 공개 후 사용하세요.
4. 상단부터 셀을 순서대로 실행합니다. Gemini 무료 웹 버전은 [gemini.google.com](https://gemini.google.com/)에서 사용합니다.
5. `docs/PROMPTS.md`를 따라 Gemini에서 프롬프트를 실행하고 `docs/WORKSHEET.md`에 결과를 작성합니다.

**대안:** GitHub Raw URL을 사용할 수 없다면 CSV 파일 두 개를 Colab 세션에 업로드한 후 첫 번째 셀의 `DATA_BASE`를 빈 문자열로 바꾸고 파일명만으로 읽도록 수정하세요. 무료 계정의 사용량·파일 업로드 제한에 대비해 **Gemini에 CSV 전체를 업로드하지 않아도** 실습할 수 있도록 설계했습니다.

## 80분 진행표
| 시간 | 활동 | 산출물 |
|---|---|---|
| 0~10분 | 품질·생산관리 직무와 생성형 AI의 역할 | 분석 목표 |
| 10~20분 | Colab 실행, 데이터 구조와 프롬프트 확인 | 데이터 점검 |
| 20~40분 | 생산 실적·품질 지표 계산 및 라인별 비교 | 지표 요약표·차트 |
| 40~60분 | 불량 유형 파레토 분석, 라인 B의 변화 탐색 | 파레토·추세 차트 |
| 60~75분 | Gemini 활용 해석, 개선 가설 및 검증 계획 | 개선 제안 |
| 75~80분 | 계산·해석 검증, 제출 | 워크시트 |

## 파일 구성
- `data/production_daily.csv`: 20일 × 3개 생산라인의 가상 생산 데이터
- `data/defect_types.csv`: 같은 기간의 불량 유형별 건수 (일자·라인별 불량 합계 일치)
- `notebooks/production_quality_workshop.ipynb`: 실행 가능한 Colab 노트북
- `docs/PROMPTS.md`: 단계별 Gemini 프롬프트
- `docs/WORKSHEET.md`: 학생 실습지
- `docs/INSTRUCTOR_GUIDE.md`: 교수자용 진행·검증 포인트

## 지표 정의 및 해석 주의
- **계획 달성률(%)** = 실제 생산량 / 계획 생산량 × 100
- **불량률(%)** = 불량 수량 / 실제 생산량 × 100 (단순 불량 수량 기준, 개별 불량품 중복 집계 없음 가정)
- **시간당 생산량** = 실제 생산량 / 실제 가동시간 (개/시간)
- **시간가동률(%)** = (계획 가동시간 − 비가동시간) / 계획 가동시간 × 100
- **집계 불량률**은 일별 불량률의 단순 평균이 아닌 `불량 수량 합 / 실제 생산량 합`으로 계산합니다.
- 시간가동률은 여기서 정의한 **가동시간 비율**이며 OEE 전체를 뜻하지 않습니다.
- 데이터는 **교육용 합성 데이터**입니다. 원인·인과관계나 통계적 관리 상태를 확정할 수 없습니다.

## 무료 사용 조건
Colab 무료 런타임 및 Gemini 무료 계정은 이용량·기능에 제한이 있을 수 있습니다. 유료 API 키, 결제 계정, 별도 설치는 요구하지 않습니다. 노트북 분석은 Gemini 접속 없이도 실행 가능합니다.

## 추가 실습: Julius AI 및 현장 문제 정의
- `docs/WHY_THIS_PRACTICE.md`: 실습의 필요성, 직무 의사결정, 80분 운영
- `docs/JULIUS_AI_PRACTICE.md`: Julius AI 무료 계정 기반 자연어 분석·시각화 및 Colab 검증
- 개정 강의 PPT: `성결대_생성형AI_생산품질_특강_개정_JuliusAI.pptx` (별도 배포)

## 학생용 Drive·GitHub 실습 안내
- `docs/STUDENT_WORKSHEET_DRIVE_GITHUB.md`: Colab 초보/경험자별 절차, GitHub 다운로드·Fork·개인 저장소 업로드, 단계별 실습
- `notebooks/production_quality_workshop_DRIVE.ipynb`: 본인 Google Drive에 업로드한 CSV를 읽는 실행용 노트북
