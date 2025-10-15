# advanced_ANN
숭실대 전자정보공학부 IT융합전공 고급인공신경망 수업 (권민혜 교수, 박희원 조교)

---

# 2025 advanced_ANN Tool Installation Guide
## 1. CoLab 활용 방법
1. 다음 링크로 구글 CoLab 접속 (https://colab.research.google.com/)
2. 새로운 Jupyter notebook 파일 생성 또는 컴퓨터에 저장된 Jupyter notebook 파일 업로드
3. [런타임]-->[런타임 유형 변경]-->T4 GPU 선택
   ![img.png](2024/img/img1.png)
4. 각 cell 실행
5. 저장하기: File -> download .jpynb -> save the file

---

## 2025 advanced_ANN Project Guide
### 주제: EMNIST dataset을 이용한 AE 기반 이상탐지 모델 최적화 및 분석
### 프로젝트 일정

|      일정       | 기한                    |
|:-------------:|:----------------------|
|    팀 빌딩 (4~5인)  | ~10월 22일 (수) 23:59 |
|    1차성능 제출    | 11월 1일 (토) 23:59 |
|    2차성능 제출     | 11월 15일 (토) 23:59 |
|     중간 보고서 제출     | 11월 18일 (화) 23:59  |
|     최종 발표     | 12/12 (금) 19:00- |
|   최종 결과물 제출   | 12/12 (금) 19:00 (최종 발표 당일) |


### 프로젝트 목표
- EMNIST dataset을 이용하여 직접 설계한 AE모델을 학습시키고 이상탐지를 위한 적절한 하이퍼파라미터 조합을 찾는다.
- 이상탐지는 EMNIST dataset을 사용하여 문자의 경우 이상, 숫자의 경우 정상으로 판단한다.

### 프로젝트 수행 방법
1. EMNIST dataset 중 숫자 데이터로 AE 모델을 학습하여 결과를 확인한다.
2. Hyperparameter 변경을 통해 최적의 AE 학습 결과를 얻는다. (변경 가능한 Hyperparameter: 모델 layer 수, node 수, learning rate, epoch, batch size, optimizer, threshold 설정, loss 함수)
3. Reconstruction error와 이상탐지 성능을 고려하여 직접 설계한 네트워크의 결과를 분석하고 성능 평가를 수행한다. 이때 모델 구조 선정 과정과 결과를 실험 및 분석 결과에 근거하여 제시한다.

**수행 과정**
- 프로젝트 예시 코드[git](https://github.com/bmil-ssu/advanced_ann/blob/main/2025/Code/Advanced_Ann_project.ipynb) - 코드 내 수정 가능 부분만 변경
- 데이터 제공 링크[git](https://github.com/bmil-ssu/advanced_ann/blob/main/2025/Dataset/Data.md) - 제공 데이터만을 사용하여 학습 및 성능 평가
- 주의사항: Google colab에서 가능한 범위 내에서만 하이퍼파리미터 튜닝 가능(개인 gpu 사용 불가)
- 모델 최적화 및 분석:
   - Model과 training hyperparameter의 최적화를 통해 최대 성능을 획득.
   - 최적화 과정 제시 및 결과 분석 -> EMNIST dataset에 포함된 validate dataset을 기반으로 한 성능 평가
   - Epoch에 따른 learning curve 제시.
   - 이상탐지 성능 지표 수식 및 결과 포함(Accuracy, Recall, Precision, F1-score) -> EMNIST dataset에 포함된 test dataset을 기반으로 한 성능 평가

### 요구 조건
1. 4~5인이 한 팀을 이루어 프로젝트 진행 (8주차 프로젝트 팀 구성 조사 게시글에 댓글 남기기 ~10/22) 
2. 팀원 수에 따른 점수 차이 없음 (결과 평가시 팀원이 몇명인지 고려 안함)
3. 제출자료: 중간보고서, 최종발표자료, 실행결과 포함한 노트북 파일. 모든 파일은 pdf와 ipynb로 제출. (최종 보고서는 없음- 발표자료로 대체)
4. 중간보고서 및 최종발표자료 포함사항
   - 하이퍼파라미터 별 성능 영향력 분석 내용
   - 이상탐지 성능 지표 설명(중요!!) 및 분석 내용 
   - (꼭 들어갈 내용) hyperparmeter1을 이렇게 변경하였더니 성능지표 A는 올라가고 성능지표 B는 내려갔다. 실제 산업계 활용을 생각하면 이러저러한 사유로 성능 A가 B보다 중요하기에 최종 hyperparameter를 이렇게 정했다.

### 평가 방식
- 중간 보고서 및 1,2차 성능 결과 평가
- 최종 발표 및 결과물 평가

### 1차성능 구글시트 제출 (11/1 (토) 23:59) -> 어느 팀의 성능 가장 좋은지 competition!!!
- 최적의 하이퍼파라미터 도출
- validate dataset을 사용한 성능 평가
- 구글 시트에 성능 입력(이상탐지 성능, loss 값 등)
- 11/3 (월) 수업시간에 성능 종합 평가(성능 랭킹 기준 점수 반영)
- latent size 변경 가능
- 1차성능 확인 후 제약조건(예: latent size)을 줄 예정 (해당 제약조건은 2차성능때엔 만족시켜야 함)
- output layer activation function은 현재 코드로 유지, hidden layer activation function은 변경 가능 (단, 모든 hidden layer 동일한 activation function 사용)

### 2차성능 구글시트 제출 (11/15 (토) 23:59) - 제약 조건: 1차 성능 평가 이후 제공 예정
- 제시된 모델 구조에 따른 최적의 하이퍼파라미터 도출
- validate, test dataset을 사용한 성능 평가
- 제약조건하에 하이퍼파리미터 튜닝 수행
- 구글 시트에 성능 입력(이상탐지 성능, loss 값 등)
- 11/17 (월) 수업시간에 성능 종합 평가 수업 진행

### 프로젝트 중간점검 보고서 제출 (11/18 (화) 23:59)
- 보고서 양식[docx](https://docs.google.com/document/d/1sC790ydDjOc1SSC0iIX1TJ7t02GId3QY/edit?usp=sharing&ouid=115661534345468656315&rtpof=true&sd=true)
포함할 사항
- 사용 하이퍼파라미터 분석 내용
- 이상탐지 성능 지표 설명 및 분석 내용
- Jupyter notebook 코랩 링크
- 2024년 우수 보고서 예시
- [예시1pdf](https://drive.google.com/file/d/1LkUXHj3FYNyKy3jL8516OAm-nX6fB0B2/view?usp=sharing)
- [예시2pdf](https://drive.google.com/file/d/1NelIp0Oba2Q0wxDQT9Z88i-UTM_-x74e/view?usp=sharing)
- [예시3pdf](https://drive.google.com/file/d/1o01QoZyTOMHjmxJT80-MRCGUYPHKScjd/view?usp=sharing)
- [예시4pdf](https://drive.google.com/file/d/1zS6WSQhIk6XPNEwh9rNeaGc2hLW2xiJW/view?usp=sharing)

### 프로젝트 최종발표 (12/12(금) 19시 -, 장소 미정)
- 6분 발표, 3분 질의 응답
- 팀별 1인 발표 or 나누어 발표 자유 (점수 차등 없음)
- 장소 추후 공지
  
### 프로젝트 최종 제출 자료 (12/12 (금) 19:00)
1) 발표자료 (최종 발표자료 pdf)
2) 실행 결과 포함한 노트북 파일
3) zip 파일로 묶어서 제출
  

