# 데이터 분석 프로젝트 모음 (2024.01 ~ 2024.07)

빅데이터 서비스 개발자 과정에서 수행한 데이터 처리/분석/모델링 실습 과제 모음입니다.

---

## 📁 프로젝트 구성

### 1. PySpark - 대용량 데이터 처리

| 파일 | 내용 |
|---|---|
| day4-01_dataframe_api.ipynb | PySpark DataFrame API 기초 (읽기/쓰기, 결측치, filter, 파티셔닝) |
| day4-02_advanced.ipynb | PySpark 심화 (groupBy, join, window function, UDF) |
| day5-01.ipynb | Spark ML 기반 머신러닝 (선형회귀, 랜덤포레스트) |
| pyspark_assignment.ipynb | PySpark 실전 과제 (9문제) |

**주요 기술**
- SparkSession 기반 대용량 데이터 처리
- groupBy / agg / orderBy 집계 처리
- join (inner, left) 을 활용한 다중 테이블 분석
- Window Function 기반 순위/누적 연산
- UDF (User Defined Function) 작성 및 적용
- regexp_extract, to_date 등 내장 함수 활용
- parquet 포맷 기반 데이터 읽기/쓰기

---

### 2. Data-Analysis - 통계 분석

| 파일 | 내용 |
|---|---|
| day5_final-report.ipynb | NYC Airbnb 가격 데이터 EDA 및 통계 분석 |

**주요 내용**
- 데이터셋: Kaggle NYC Airbnb Open Data (48,895건)
- 분석 목표: 숙박 가격(price)과 최소 숙박일수(minimum_nights) 간 상관관계 검증
- 수행 기법
  - Pandas EDA (결측치, 중복값, 기술통계)
  - Pearson 상관분석 (r = 0.04, p < 0.05)
  - 선형회귀 모델링 (statsmodels OLS)
  - 가설검정 (독립표본 t-test, Cohen's d 효과 크기 분석)
  - seaborn / matplotlib 시각화
- 결론: 통계적 유의미성은 확인되나 실질적 효과 크기는 작음

---

### 3. 이미지 분석 모델 성능 지표 분석 - 딥러닝 실험

| 파일 | 내용 |
|---|---|
| [FIN]image_proj_AUG_50.ipynb | 데이터 증강 O / 이미지 크기 50×50 |
| [FIN]image_proj_AUG_100.ipynb | 데이터 증강 O / 이미지 크기 100×100 |
| [FIN]image_proj_NO_AUG_50.ipynb | 데이터 증강 X / 이미지 크기 50×50 |
| [FIN]image_proj_NO_AUG_100.ipynb | 데이터 증강 X / 이미지 크기 100×100 |
| image_proj_AUG_100_RESULT.ipynb | 최종 결과 비교 |

**주요 내용**
- 과제 목표: 얼굴 이미지로 나이대(18개 클래스) 분류
- 실험 변수: 이미지 크기(50×50 vs 100×100) × 데이터 증강 여부(AUG vs NO_AUG)
- 모델: ResNet18, VGG13, GoogLeNet
- 옵티마이저: SGD, RMSprop, AdamW 비교
- 프레임워크: PyTorch
- 기타: Early Stopping, OpenCV 기반 데이터 증강 구현

---

## 🛠 사용 기술 스택

| 분야 | 기술 |
|---|---|
| 대용량 데이터 처리 | PySpark, Parquet |
| 데이터 분석 | Pandas, NumPy, SciPy, statsmodels |
| 시각화 | matplotlib, seaborn |
| 딥러닝 | PyTorch, torchvision, OpenCV |
| 환경 | Python 3, Jupyter Notebook, Google Colab |
