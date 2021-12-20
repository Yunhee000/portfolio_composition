# 로보어드바이저 알고리즘을 활용한 포트폴리오 구성 \n (Capstone Design 2021-2)
* 소프트웨어융합학과 2019102084 김윤희
## Overview
* **Needs**
  * 최근 로보어드바이저와 관련된 금융상품들이 출시되고 있는데 로보어드바이저는 인간의 주관적 판단이나 개입이 없이 알고리즘을 사용해 포트폴리오를 제시하는 자산 관리 로봇이다.
  * 기계가 자산 관리를 해주면서 소액투자자들에게도 서비스를 제공하기 시작하면서 많은 사람들이 사용하고 있다.
  * 로보 어드바이저 알고리즘을 활용하여 효용을 극대화할 수 있는 포토폴리오를 찾을 수 있다.
* **Goals**
  * 예측기를 사용하여 포트폴리오의 투자 비중을 결정하는데 이 때 구한 비중으로 총 수익률이 0% 이상이어야 한다.
  * 위험 대비 수익률의 지표인 샤프지수가 0.1 이상이 되도록 해야 한다.
## Schedule
|Contents|Sep|Oct|Nov|Dec|Progress|
|---|---|---|---|---|---|
|논문 리뷰|✓|||✓||
|주가 데이터 확보|✓|✓||||
|주가 데이터 시각화||✓||||
|블랙리터만 모델 구현||✓||||
|SVM 활용 투자자 전망||✓|✓|||
|LSTM 활용 투자자 전망|||✓|✓|중간발표.ipynb|
|GRU 활용 투자자 전망||||✓||
|결과 분석||||✓||
## Results
* 데이터
한국거래소가 발표한 KOSPI 200의 구성종목을 산업군별로 재분류하여 발표하고 있는 10개의 섹터지수를 사용하였다.
-건설, 중공업, 철강/소재, 에너지/화학, 정보기술, 금융, 생활소비재, 경기소비재, 산업재, 헬스케어
  <img width="636" alt="스크린샷_2021-12-16_오후_3 39 52" src="https://user-images.githubusercontent.com/87518915/146711528-b0f0d244-a36a-46a6-9bd0-a24eb2a95d06.png">
* 평균분산모형과 블랙리터만 모형의 비교
평균분산모형의 특정 자산군에 집중되는 코너해 문제와 입력변수에 민감한 문제를 해결하면서 투자자 전망을 결합한 모델이 블랙리터만 모델이다.
  <img width="616" alt="스크린샷 2021-11-04 오전 2 19 23" src="https://user-images.githubusercontent.com/87518915/140437704-c0151538-8063-40be-9017-055944ae9460.png">
평균분산모형으로 구한 포트폴리오의 투자 비중과 블랙리터만 모형의 투자 비중을 비교하면 특정 자산군에 집중되어 있는 평균분산 모형의 코너해 문제를 해결한 것을 확인할 수 있다.
* 예측기로 SVM을 사용한 투자자 전망
  
## Conclusion
*
## Reports
* Midterm : [report](https://github.com/Yunhee000/portfolio_composition/blob/main/report/2019102084_%E1%84%80%E1%85%B5%E1%86%B7%E1%84%8B%E1%85%B2%E1%86%AB%E1%84%92%E1%85%B4_%E1%84%8C%E1%85%AE%E1%86%BC%E1%84%80%E1%85%A1%E1%86%AB%E1%84%87%E1%85%A1%E1%86%AF%E1%84%91%E1%85%AD.pdf)
* Final : 
