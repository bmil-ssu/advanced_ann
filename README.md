# advanced_ANN
숭실대 전자정보공학부 IT융합전공 고급인공신경망 수업 (권민혜 교수, 조무곤 조교)

---

# 2024 advanced_ANN Tool Installation Guide
## 1. CoLab 활용 방법
1. 다음 링크로 구글 CoLab 접속 (https://colab.research.google.com/)
2. 새로운 Jupyter notebook 파일 생성 또는 컴퓨터에 저장된 Jupyter notebook 파일 업로드
3. [런타임]-->[런타임 유형 변경]-->T4 GPU 선택
   ![img.png](2024/img/img1.png)
4. 각 cell 실행
5. 저장하기: File -> download .jpynb -> save the file

---

## 2024 advanced_ANN Project Guide
### 주제: EMNIST dataset을 이용한 AE 기반 이상탐지 모델 최적화 및 분석
### 프로젝트 일정

|      일정       | 기한                    |
|:-------------:|:----------------------|
|    1차성능 구글시트 제출    | 10월 29일 (화) 23:59 |
|    2차성능 구글시트 제출     | 11월 5일 (화) 23:59 |
|     중간 보고서 제출     | 11월 5일 (화) 23:59 |
|   최종 결과물 제출   | 11/24 (일) 23:59 |
|     최종 발표     | 11/25 (월) 시간 추후 결정 |

### 프로젝트 목표
- EMNIST dataset을 이용하여 직접 설계한 AE모델을 학습시키고 이상탐지를 위한 적절한 하이퍼파라미터 조합을 찾는다.
- 이상탐지는 EMNIST dataset을 사용하여 문자의 경우 이상, 숫자의 경우 정상으로 판단한다.

### 프로젝트 수행 방법
1. EMNIST dataset을 분석하고, 숫자 데이터로 AE 모델을 학습하여 결과를 확인한다.
2. Hyperparameter 변경을 통해 최적의 AE 학습 결과를 얻는다. (Hyperparameter: 모델 layer 수, node 수, learning rate, epoch, batch size, optimizer, threshold 설정)
3. Reconstruction error와 이상탐지 성능을 고려하여 직접 설계한 네트워크의 결과를 분석하고 성능 평가를 수행한다. 이때 모델 구조 선정 과정과 결과를 실험 및 분석 결과에 근거하여 제시한다.

**수행 과정**
- 프로젝트 예시 코드[git](https://github.com/bmil-ssu/advanced_ann/blob/main/2024/Code/Advanced_Ann_project.ipynb) - 코드 내 수정 가능 부분만 변경
- 데이터 제공 링크[git](https://github.com/bmil-ssu/advanced_ann/blob/main/2024/Dataset/Data.md) - 제공 데이터만을 사용하여 학습 및 성능 평가
- 주의사항: Google colab에서 가능한 범위 내에서만 하이퍼파리미터 튜닝 가능(개인 gpu 사용 불가)
- 모델 최적화 및 분석:
   - Model과 training hyperparameter의 최적화를 통해 최대 성능을 획득.
   - 최적화 과정 제시 및 결과 분석 -> EMNIST dataset에 포함된 valid dataset을 기반으로 한 성능 평가
   - Epoch에 따른 learning curve 제시.
   - 이상탐지 성능 지표 수식 및 결과 포함 -> EMNIST dataset에 포함된 test dataset을 기반으로 한 성능 평가

### 요구 조건
1. 1인 또는 2인 프로젝트
2. 제출자료: 중간보고서, 발표자료, 실행결과 포함한 노트북 파일. 모든 파일은 pdf와 ipynb로 제출.
3. 보고서 및 발표자료 포함사항
   - 하이퍼 파라미터 별 성능 영향력 분석 내용
   - 이상탐지 성능 지표 설명 및 분석 내용

### 평가 방식
- 중간 보고서 및 1,2차 성능 결과 평가
- 최종 발표 및 결과물 평가

### 1차성능 구글시트 제출 (10/29 (화) 23:59)
- 최적의 하이퍼파라미터 도출
- valid dataset을 사용한 성능 평가
- 구글 시트에 성능 입력(이상탐지 성능, loss 값)[sheet](https://docs.google.com/spreadsheets/d/1s1Ylj7ZBZPjnHhEU7gBR7HI9Xdqe584pd9LaUTmBwHc/edit?usp=sharing)
- 10/30 (수) 수업시간에 성능 종합 평가(점수 반영)

### 2차성능 구글시트 제출 (11/5 (화) 23:59)
- 제시된 모델 구조에 따른 최적의 하이퍼파라미터 도출
- valid, test dataset을 사용한 성능 평가
- 제시된 조건하에 하이퍼파리미터 튜닝 수행(latent size, layer 수 등)
- 구글 시트에 성능 입력(이상탐지 성능, loss 값)[sheet](https://docs.google.com/spreadsheets/d/1s1Ylj7ZBZPjnHhEU7gBR7HI9Xdqe584pd9LaUTmBwHc/edit?usp=sharing)

### 프로젝트 중간점검 보고서 제출 (11/5 (화) 23:59)
- 보고서 양식[docx](https://docs.google.com/document/d/1sC790ydDjOc1SSC0iIX1TJ7t02GId3QY/edit?usp=sharing&ouid=115661534345468656315&rtpof=true&sd=true)
포함할 사항
- 사용 하이퍼파라미터 분석 내용
- 이상탐지 성능 지표 설명 및 분석 내용
- Jupyter notebook 코랩 링크
- 우수 보고서 예시
- [pdf](https://canvas.ssu.ac.kr/courses/23813/files/2261965/download?wrap=1)
- [pdf](https://canvas.ssu.ac.kr/courses/23813/files/2261964/download?wrap=1)
- [pdf](https://canvas.ssu.ac.kr/courses/23813/files/2261966/download?wrap=1)

### 프로젝트 최종발표 (11/25 (월) 시간 추후 결정)
- 발표자료 교수석 컴퓨터에 넣어놓을 것 (혹은 개인 랩탑 연걸 테스트 할것) 
- 인당 10분발표 (시간 엄수)
포함할 사항
- 프로젝트 최종결과
- 하이퍼파라미터에 따른 성능 변화
- 최종 정량적 이상탐지 성능
- (중요)프로젝트 수행과정에서 나타난 challenges & solutions
- (중요)lessons learned

### 프로젝트 최종 제출 자료 (11/24 (일) 23:59)
1) 발표자료 (최종 발표자료 pdf)
2) 실행 결과 포함한 노트북 파일
3) zip 파일로 묶어서 제출
  

