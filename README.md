# Traffic Accident Python Analysis — 교통사고 통계 분석

연도별 교통사고 통계 데이터를 활용한 Python 기반 데이터 분석 프로젝트입니다.
사고건수·사망자수·부상자수 간의 관계를 상관분석으로 확인하고, 회귀·PCA·시계열(ARIMA) 모델로 예측까지 수행했습니다.

- **형태**: 개인 프로젝트
- **환경**: Jupyter Notebook

---

## 분석 파이프라인

```
데이터 정제 → 상관관계 분석 → 선형회귀 예측 → PCA 차원 축소 → ARIMA 시계열 예측 → 시각화
```

### 1. 데이터 정제
- 원본 CSV의 수치형 컬럼 변환 및 결측 처리

### 2. 상관관계 분석
- **피어슨 / 스피어만 / 켄달** 세 가지 상관계수를 모두 계산해 비교
- 사고건수–부상자수–사망자수 간 상관 구조 확인

### 3. 선형회귀
- 사고 지표를 설명변수로 **부상자수 예측** 모델 구성
- 회귀계수와 결정계수로 설명력 해석

### 4. PCA (주성분 분석)
- 여러 사고 지표를 주성분으로 축소해 데이터의 주요 변동 방향 확인

### 5. ARIMA 시계열 분석
- 연도별 **사고건수 추세를 시계열 모델로 예측**
- statsmodels 기반 모델 적합 및 예측 구간 시각화

---

## 기술 스택

| 구분 | 기술 |
|------|------|
| Language | Python |
| 환경 | Jupyter Notebook |
| 데이터 처리 | pandas |
| 시각화 | matplotlib |
| 모델링 | scikit-learn (회귀, PCA), statsmodels (ARIMA) |

---

## 파일 구조

```text
notebooks/
└── traffic_accident_analysis.ipynb        분석 노트북 (전체 파이프라인)
presentation/
└── traffic_accident_analysis_presentation.pptx   발표 자료
data/
└── lsh2024000629.csv                      원본 데이터 (재실행 시 필요)
```

---

## 실행 방법

```bash
pip install -r requirements.txt
jupyter notebook notebooks/traffic_accident_analysis.ipynb
```

> 노트북을 다시 실행하려면 `data/lsh2024000629.csv` 원본 데이터 파일이 필요합니다.

---

## 배운 점

하나의 데이터셋에 상관분석·회귀·차원축소·시계열까지 서로 다른 접근을 적용하며, **분석 목적에 따라 방법을 선택하는 기준**을 익혔습니다. 특히 세 가지 상관계수를 비교하면서 데이터 분포에 따라 적합한 지표가 달라진다는 점, 시계열 예측은 추세·계절성 가정 확인이 선행되어야 한다는 점을 배웠습니다.
