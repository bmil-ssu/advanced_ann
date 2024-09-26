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
### 주제: MNIST dataset을 이용한 AE 기반 이상탐지 모델 최적화 및 분석
### 프로젝트 일정

|      일정       | 기한                    |
|:-------------:|:----------------------|
| 프로젝트 수행계획서 제출 | ?월 ?일 23:59       |
|     중간 점검     | ?월 ?일(?주차 수업시간) |
|   최종 결과물 제출   | ?월 ?일 23:59      |
|     최종 발표     | ?월 ?일 6:00-9:00P.M.|

### 프로젝트 목표
MNIST dataset을 이용하여 직접 설계한 AE모델을 학습시키고 이상탐지를 위한 적절한 하이퍼파라미터 조합을 찾는다.
이상탐지는 EMNIST dataset을 사용하여 문자의 경우 이상, 숫자의 경우 정상으로 판단한다.

### 프로젝트 수행 방법
1. MNIST dataset을 분석하고, AE 모델을 학습하여 결과를 확인한다. - baseline 설정 (baseline은 연구에서 새로운 모델이나 방법의 성능을 객관적으로 평가하기 위한 기준점으로 사용되는 모델이나 알고리즘을 뜻함)
2. Hyperparameter 변경을 통해 최적의 학습 결과를 얻는다. 
3. Reconstruction error와 이상탐지 성능을 고려하여 직접 설계한 네트워크의 결과를 분석한다. 이때 모델 구조 선정 과정과 결과를 실험 및 분석 결과에 근거하여 제시한다.

**수행 과정**
1) MNIST dataset 개요 및 분석: (Get the data/Discover and visualize the data) - 데이터 전처리 근거 제시
2) Dataset 분류: training/validation dataset으로 분배 (Prepare the data)
3) Baseline 학습 및 결과분석 (Reconstruction error 확인)
4) 모델 최적화 및 분석:
   - Model과 training hyperparameter의 최적화를 통해 최대 성능을 획득.
   - 최적화 과정 제시 및 결과 분석. 학습시간, 예측시간(inference time), 정확도 측면에서 분석 -> EMNIST dataset에 포함된 test dataset을 기반으로 한 성능 평가: 주어
   진 dataset에 대한 학습 최적화 결과 평가
   - Epoch에 따른 learning curve 제시.
   - 학습 dataset 선택을 포함 한 전반적인 AE 개발 결과에 대한 평가(Fine tune the model)

### 요구 조건
1. 1인 팀프로젝트
2. 프로젝트 수행계획을 세우고 업무마다 역할 분담: 프로젝트 수행계획서 제출
3. 프로젝트 수행일지 작성
4. 제출자료: 수행계획서, 보고서, 발표자료, 실행결과 포함한 노트북 파일. 모든 파일은
pdf와 ipynb로 제출 (팀당 1개씩).
5. 보고서 및 발표자료 포함사항
   - 프로젝트 개요 및 목표
   - 수행계획 및 역할 분담 (수정한 계획 및 역할 요약)
   - 프로젝트 수행과정 (최종 정량적 성능, 프로젝트 수행과정에서 나타난 challenges & solutions, lessons learned) 
   - 결론

### 평가 방식
- 보고서 및 시뮬레이션 결과 평가
- 문제의 분석과 solution 도출 과정이 나타나야 함
    
### 프로젝트 중간점검 (?/? 수업시간 12시-1시15분)
- MNIST dataset 개요 및 분석, Dataset 분류, Baseline 학습 및 결과분석
포함할 사항
- 지금까지 프로젝트 진행사항
- 현재의 정량적 성능
- 남은 기간 계획

### 프로젝트 최종발표 (?/? 6-9PM)
- 최종 발표 평가표[docx](https://docs.google.com/document/d/1y5m70j2Ep6aQyiIQzUXTUXCFIeotviSL/edit?usp=sharing&ouid=115661534345468656315&rtpof=true&sd=true)
- ?시까지 발표자료 교수석 컴퓨터에 넣어놓을 것 (혹은 개인 랩탑 연걸 테스트 할것) 
- 인당 ?분발표 (시간 엄수)
포함할 사항
- 프로젝트 최종결과
- 최종 정량적 이상탐지 성능
- (중요)프로젝트 수행과정에서 나타난 challenges & solutions
- (중요)lessons learned

### 프로젝트 최종 제출 자료 (due ?/? 11:59 P.M)
1) 최종 보고서
  - **A4 5페이지 이내(표지 및 참고문헌 제외)** 폰트 및 여백은 **가독성을 고려**하여 적절히 자유롭게 설정 가능
2) 발표자료 (중간, 최종 발표자료 pdf)
3) 수행 계획서
4) 실행 결과 포함한 노트북 파일
1)~4) zip 파일로 묶어서 제출
  

