# ML_portfolio

## Table of Contents

 1. 제주 도로교통량 
 2. Cook County Tax appeal Process
 3. Cook County Tax appeal Process 2
 4. 농수산 가격 예측 AI
 5. 던전 앤 파이터즈 EDA
 
## 제주 도로교통량(With 전주혁, 최다희, 곽명빈, 새한)
  1. Objective
    
    -제주도 도로 교통량 예측 AI 알고리즘 개발
    -MAE를 기준으로 target column을 예측하는 희귀 예측 모형 개발
    
  2. About the Dataset
  
    1)주어진 데이터:
    
      -2022년 8월 이전의 제주도 도로 교통량 데이터
      -4701217개의 row개수와 23개의 columns(ID,target제외)
      -target값
      
    2)사용한 외부 데이터
    
      -공휴일 데이터
      -서귀포시, 제주시, 성산일출봉, 한라산, 중문 위도와 경도
      -관광지 데이터(2022년 8월 이전 데이터)
      
  3. Model
   
    -Xgboost + Optuna(hyperparameters tuning)
    
  4. 성과
   
    -LB score 4위
    
  5. 아쉬운 점
   
    1)Feature Selection 데이터셋의 사이즈가 너무 커서 rfe, sharplee, Boruta, permutation 등의 방법을 활용하기가 어려웠음 
    2)더 다양한 외부데이터 활용 가능성 ex)카카오 api(데이터 갱신 시점을 알기 어려워 활용x)

## Cook County Tax appeal Process
  1. Objective
   
   To understand,
   
   1) What variables influence whether a property owner appeals?
   2) What influences the monetary reduction they gain from appeal?
    
   to know whether there exists unfairness or bias.
  
  2. PART 2 - Predictors of Appeal Reduction and Fairness를 맡아서 진행
   
   3가지 가설의 검증에 초점을 맞추고 진행(OLS regression를 활용)
   
   1) As AV/MV(assessed value to maket value ratio) increases, monetary award would increase.
   2) high income, majority white neighbors tend to get advantage on getting appeal.
   3) region would matter.
   
  3.아쉬운 점
   
   1) Monetary Amount 에 대한 정의가 단순했던 점
   2) 만든 모델들의 설명력이 너무 낮았다는 점
   
## Cook County Tax appeal Process

  1.Objective
  
   1)
   
   
   
   
   
## 농수산 가격 예측 AI

 1.Obejective
  
  -농산물 가격 변동률 예측 AI 모델 개발
  -평가지표: MAE
  
 2.About the Dataset
  
  -37개 품목에 대한 시계열 데이터
  -raw데이터는 품목별 날씨, 품목별 가격, 품목별 도매 데이터, 품목별 소매 데이터, 품목별 무역 수출입 기록 등으로 이루어진 데이터
  
 3.MODEL
  
  -NHITS 모델(pytorch forecast)활용
  
 4.아쉬운 점
 
  -hyperparameters tuning을 못한점
  -Feature Selection?
  
  
## 던전앤파이터즈 EDA

 1.Objective
  PC 던전 앤 파이터즈 게임에 대한 유저들의 관심사를 알기 위한 EDA
 
 2.Method
  던파 유저들의 트래픽이 몰리는 커뮤니티들(던파조선, DC던전앤파이터즈 갤러리) 크롤링 후, token화 하여 token frequency를 시각화
  
  
