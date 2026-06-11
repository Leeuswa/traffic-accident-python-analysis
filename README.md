# Traffic Accident Python Analysis

교통사고 통계 데이터를 활용한 Python 기반 데이터 분석 프로젝트입니다.

## 분석 주제

연도별 교통사고 지표를 활용하여 사고건수, 사망자수, 부상자수 사이의 관계를 분석하고 예측 모델을 구성했습니다.

## 분석 내용

- 데이터 정제 및 수치형 컬럼 변환
- 피어슨, 스피어만, 켄달 상관관계 분석
- 선형회귀를 통한 부상자수 예측
- PCA 주성분 분석
- ARIMA 시계열 분석을 통한 사고건수 예측
- 분석 결과 시각화

## 기술 스택

- Python
- Jupyter Notebook
- pandas
- matplotlib
- scikit-learn
- statsmodels

## 파일 구조

```text
notebooks/
└── traffic_accident_analysis.ipynb

presentation/
└── traffic_accident_analysis_presentation.pptx

data/
└── lsh2024000629.csv
```

## 실행 방법

필요 패키지 설치:

```bash
pip install -r requirements.txt
```

Jupyter Notebook 실행:

```bash
jupyter notebook notebooks/traffic_accident_analysis.ipynb
```

## 주의

현재 저장소에는 노트북과 발표자료가 포함되어 있습니다.  
노트북을 다시 실행하려면 `data/lsh2024000629.csv` 원본 데이터 파일을 추가해야 합니다.
