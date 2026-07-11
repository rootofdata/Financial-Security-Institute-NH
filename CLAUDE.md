# 프로젝트
금융보안원 NH 경진대회: 온라인 품목별 소비 데이터(BC카드)와 주가지수의 상관관계를 분석하고 회귀 모델로 주가 방향성을 예측하는 데이터 분석 프로젝트.

# 환경·실행
- 언어: Python 3 (Jupyter Notebook)
- 주요 패키지: `pandas`, `numpy`, `scikit-learn`(RandomForestRegressor, GridSearchCV, PCA, StandardScaler, train_test_split), `xgboost`, `lightgbm`, `matplotlib`, `seaborn`
- 실행: `jupyter notebook`으로 각 주제 폴더의 노트북을 파이프라인 순서(KRX → Upsampling → Classifier/Modeling → Visualization)대로 실행. requirements 파일 없음 → 패키지 개별 설치.
- 데이터 위치: **저장소에 원본 데이터 없음.** 노트북들이 하드코딩된 로컬 절대경로(예: `C:/Users/dudtj/OneDrive/Desktop/python/금융데이터/...`, `금융보안원_경진대회_데이터`)를 참조한다. 실행하려면 경로를 본인 환경에 맞게 수정해야 한다.
- 한글 폰트: matplotlib에 OS별 한글 폰트 설정 코드가 있음(Windows `malgun.ttf`, Mac `AppleGothic`). 환경에 맞게 조정.

# 폴더 구조
- 주제별 폴더: `e상품서비스/`, `식품/`, `여가스포츠/`, `전자/` — 4개 대분류 각각의 분석 노트북 세트.
- `Category/` — 대분류 도출, KRX 시세, 시각화, 회귀 관련 노트북.
- `Final.ipynb`, `Report.ipynb` — 최종 통합 분석·리포트.
- `photo/` — 상관분석·시각화 결과 이미지(한글 파일명).
- `README.md` / `README(KR).md` — 프로젝트 배경·결과 요약(영문/국문).

# 컨벤션
- 주제 폴더 안의 노트북은 접두어로 단계를 표기: `KRX_`(시세 수집), `Upsampling_`(데이터 증강), `Classifier_`/`Modeling_`(모델링), `Visualization_`(시각화).
- 파일·폴더명에 한글 대분류명을 그대로 사용.
- KRX CSV 로드 시 인코딩은 `cp949`(또는 `euc-kr`)를 사용.

# 주의
- 절대경로 하드코딩이 만연하다. 노트북을 옮기거나 다른 환경에서 돌릴 때 `read_csv`/`read_excel` 경로를 반드시 수정. 상대경로로 리팩터링 시 참조가 깨지지 않는지 확인.
- KRX/한글 CSV는 UTF-8이 아니라 `cp949`이므로 인코딩 미지정 시 오류·깨짐 발생.
- 주제 폴더마다 유사 구조의 노트북이 반복되므로, 한 폴더를 수정하면 나머지 3개도 동일 패턴인지 확인.
- 대용량 데이터·캐시(`.ipynb_checkpoints`)를 커밋하지 말 것. `photo/`의 기존 이미지·데이터를 삭제하지 말 것.
- 한글 파일명은 NFC로 통일(macOS 생성 시 NFD 혼입 주의).
