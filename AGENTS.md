# AGENTS.md

AI 코딩 에이전트 및 범용 도구를 위한 가이드. 금융보안원 NH 경진대회 프로젝트: 온라인 품목별 소비 데이터(BC카드)와 주가지수의 상관관계 분석 및 주가 방향성 예측 회귀 모델.

## 명령어
- 실행: `jupyter notebook` 후 주제 폴더 노트북을 파이프라인 순서(KRX → Upsampling → Classifier/Modeling → Visualization)대로 실행.
- 의존성: 고정된 requirements 파일 없음. 필요한 패키지를 `pip install`로 개별 설치.
- 주요 패키지: `pandas`, `numpy`, `scikit-learn`, `xgboost`, `lightgbm`, `matplotlib`, `seaborn`.

## 프로젝트 개요
- 언어: Python 3 (Jupyter Notebook).
- 4개 소비 대분류(e상품서비스·식품·여가스포츠·전자)별로 KRX 시세와 소비 데이터를 결합, PCA로 다중공선성 처리 후 회귀(RandomForest/XGB/LGBM 등)로 주가지수 예측.

## 구조
- 주제 폴더: `e상품서비스/`, `식품/`, `여가스포츠/`, `전자/` — 대분류별 노트북 세트.
- `Category/` — 대분류 도출·KRX 시세·시각화·회귀 노트북.
- `Final.ipynb`, `Report.ipynb` — 최종 통합 분석·리포트.
- `photo/` — 결과 이미지(한글 파일명).

## 데이터
- **저장소에 원본 데이터 없음.** 노트북이 하드코딩된 로컬 절대경로(예: `C:/Users/dudtj/.../금융데이터/...`)를 참조하므로 본인 환경 경로로 수정 필요.
- KRX/한글 CSV 인코딩은 `cp949`(또는 `euc-kr`). 미지정 시 깨짐 발생.
- matplotlib 한글 폰트: Windows `malgun.ttf`, Mac `AppleGothic`.

## 규칙
- 노트북 접두어로 단계 표기: `KRX_`, `Upsampling_`, `Classifier_`/`Modeling_`, `Visualization_`.
- 절대경로 하드코딩 다수 → 이동·리팩터링 시 `read_csv`/`read_excel` 경로 반드시 확인.
- 한 주제 폴더 수정 시 나머지 3개 동일 패턴 확인.
- 대용량 데이터·캐시(`.ipynb_checkpoints`) 커밋 금지, `photo/` 기존 파일 삭제 금지.
- 한글 파일명은 NFC로 통일.
