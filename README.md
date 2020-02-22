## Predicting Delisting Company with ML Models


**1. Summary**
 - 1994년 ~ 2019년 코스피시장에 상장되어 있거나 상장폐지된 기업의 재무비율 및 시가총액 등의 시장데이터(출처 : DataGuide, KRX)
 - 연도별 기업들의 자기자본비율, 부채비율, 자기자본비율 유보율 등 총 24개 Features
 - Target feature는 상장폐지기업의 경우 "1", 상장기업의 경우 "0" 으로 Labeling


**2. Objective**
 - 1994년 ~ 2019년 코스피시장에 상장되어 있거나 상장폐지된 기업의 재무비율 및 시가총액 등의 시장데이터(출처 : DataGuide, KRX)
 - 연도별 기업들의 자기자본비율, 부채비율, 자기자본비율 유보율 등 총 24개 Features
 - Target feature는 상장폐지기업의 경우 "1", 상장기업의 경우 "0" 으로 Labeling


**3. Data set**
 - 1994년 ~ 2019년 코스피시장에 상장되어 있거나 상장폐지된 기업의 재무비율 및 시가총액 등의 시장데이터(출처 : DataGuide, KRX)
 - 연도별 기업들의 자기자본비율, 부채비율, 자기자본비율 유보율 등 총 24개 Features로 구성
 - Target feature는 상장폐지기업의 경우 "1", 상장기업의 경우 "0" 으로 Labeling
 

**4. Preprocessing & Feature Eng.** 
 - "N/A" 또는 "자본잠식"등 문자형으로 표시된 값을 각 feature별 특성을 감안한 값으로 대체(ex: 자기자본비율이 "완전잠식"값일 경우 -1로 대체)
 - 부채비율, 차입금비율 등의 결측값은 Target class(1 또는 0)별 평균값으로 대체
 - 상관관계가 0.95 이상변수 제외
 - RandomForest & XGBoost Classifier를 이용하여 각 features들의 중요도를 산출
 - 1년전 시가총액과 차입부채조달금리의 중요도가 타 features대비 상대적으로 높음 
 - features importance
  
  ![dataset](./fi.jpg)
 
**5. Model tunning**
 - 상장유지 종목대비 상장폐지종목수의 과소 -> Target value의 불균형 해소(Random over-sampling)
 - train set은 75, test set은 25로 분리하여 진랭
 - Logistic Regression, Decision tree, RandomForest, Adaboost, Gredient Boost, XGBoost 
 - Sklean패키지의 GridSearchCV를 이용하여 각 알고리즘별 최적 파라미터 산출 
 
 
**6. Result**

 - sdkjsdkj
 

