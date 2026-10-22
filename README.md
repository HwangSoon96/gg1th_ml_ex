<div align="center">

# gg1th_ml_ex

**scikit-learn 지도학습 실습 — 회귀 · 분류 모델 학습과 평가**

![Python](https://img.shields.io/badge/Python-3.12-3776AB?logo=python&logoColor=white)
![uv](https://img.shields.io/badge/uv-package%20manager-DE5FE9?logo=uv&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189FDD)
![LightGBM](https://img.shields.io/badge/LightGBM-02569B)

</div>

<br>

## 실습 구성

> 파일명 접미사 `a` = 강의 실습, `b` = 직접 해결 실습

### 기본

| 파일 | 내용 |
|---|---|
| `1-0a ... linear_regression_height_weight_pred` | 키 → 몸무게 회귀, train / test 분할 |
| `1-1a ... Machine Learning and Data Preprocessing` | 일반화 · 과대적합, 결측치 처리, 레이블 · 원핫 인코딩, 피처 스케일링 |

### 회귀

| 파일 | 내용 |
|---|---|
| `1-2b ... Linear Regression_basic` | 경력 → 연봉 단순 선형 회귀, 오차와 학습의 의미 |
| `2-1a ... Multiple Linear Regression` | 다중 선형 회귀 (50 Startups), 범주형 변수 처리, 모델 저장 |
| `2-2b ... 실습 linear regression` | 회귀 예측 모델 직접 구현 · 검증 |

### 분류

| 파일 | 내용 |
|---|---|
| `3-1a ... Logistic Regression` | 시그모이드, 이메일 클릭 여부 분류 |
| `3-2b ... 실습 Logistic Regression` | 불균형 데이터 업샘플링, 피처 스케일링 |
| `4a ... Decision Tree` | 결정트리 시각화, 랜덤포레스트 · XGBoost · LightGBM 비교 |
| `5a ... K-NN` | 유클리드 거리 기반 K-최근접 이웃 |
| `6a ... Support Vector Machine` | 최대 마진 분류기 |
| `7-1a ... Random_Forest (Rain in Australia)` | 내일 비 예측 — EDA → 전처리 → 랜덤포레스트 |
| `7-2a ... Random_Forest ... _Outlier 제거` | 이상치 제거 전 · 후 성능 비교 |
| `8a ... Classification_XGBoost_stroke_patient_GSCV` | 뇌졸중 환자 분류, GridSearchCV 하이퍼파라미터 튜닝 |

### 종합

| 파일 | 내용 |
|---|---|
| `9a[종합실습]` | 수질 데이터로 음용 가능 여부 판단 — EDA → 전처리 → KNN · XGBoost (GridSearchCV) → feature importance |

데이터는 `datas_ml/`, 학습된 모델은 `models/`에 포함

<br>

## 시작하기

```bash
git clone https://github.com/HwangSoon96/gg1th_ml_ex.git
cd gg1th_ml_ex

uv sync
```

VS Code 또는 Jupyter에서 `.venv` 커널을 선택해 노트북 실행

### 그래프 한글 폰트 (WSL2 Ubuntu)

```bash
sudo apt install fonts-nanum
rm -rf ~/.cache/matplotlib
```

```python
import platform
import matplotlib.pyplot as plt
from matplotlib import rc

plt.rcParams["axes.unicode_minus"] = False
rc("font", family="NanumGothic" if platform.system() == "Linux" else "Malgun Gothic")
```
