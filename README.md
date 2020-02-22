## Predicting Delisting Company with ML Models


**1. Summary**

**2. Objective**

**3. Data set**

 - 1994년 ~ 2019년 코스피시장에 상장되어 있거나 상장폐지된 기업의 재무비율 및 시가총액 등의 시장데이터(출처 : DataGuide, KRX)
 - 연도별 기업들의 자기자본비율, 부채비율, 자기자본비율 유보율 등 총 24개 Features
 - Target feature는 상장폐지기업의 경우 "1", 상장기업의 경우 "0" 으로 Labeling

**3. Preprocessing & Feature Eng.** 
 - "N/A" 또는 "자본잠식"등 문자형으로 표시된 값을 각 feature별 특성을 감안한 float 형태의 값으로 대체(ex: 자기자본비율이 "완전잠식"값일 경우 -1로 대체)
 - 
 
**4 Model tuning**
 - 생성한 난수(Random Data)를 입력 변수로 사용한 결과값과 비교하여 알고리즘의 정확도 평가

**5 Results**
 - 생성한 난수(Random Data)를 입력 변수로 사용한 결과값과 비교하여 알고리즘의 정확도 평가
 


