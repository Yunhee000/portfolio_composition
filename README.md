# 로보어드바이저 알고리즘을 활용한 포트폴리오 구성<br>(Capstone Design 2021-2)
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
* **데이터**<br>
한국거래소가 발표한 KOSPI 200의 구성종목을 산업군별로 재분류하여 발표하고 있는 10개의 섹터지수를 사용하였다.<br>
-건설, 중공업, 철강/소재, 에너지/화학, 정보기술, 금융, 생활소비재, 경기소비재, 산업재, 헬스케어
<img width="636" alt="스크린샷_2021-12-16_오후_3 39 52" src="https://user-images.githubusercontent.com/87518915/146712207-8ca5f65b-926e-422f-bea6-fe1903018e6b.png">
* 평균분산모형과 블랙리터만 모형의 비교<br>
평균분산모형의 특정 자산군에 집중되는 코너해 문제와 입력변수에 민감한 문제를 해결하면서 투자자 전망을 결합한 모델이 블랙리터만 모델이다.
<img width="697" alt="스크린샷 2021-12-16 오후 3 22 43" src="https://user-images.githubusercontent.com/87518915/146712384-9f10d3c1-131a-4b3d-b6db-0e73cd3d9939.png">
* **예측기로 SVM을 사용한 투자자 전망**<br>
  * 실제 값을 이용한 예측
    다음 달의 수익률 상승, 하락을 예측하는데 이전 예측 값이 아닌 실제 값을 사용했을 때의 포트폴리오 투자 수익률을 구해보았다.
    <img width="330" alt="스크린샷 2021-12-16 오후 4 21 56" src="https://user-images.githubusercontent.com/87518915/146782137-2f595671-1aab-45c9-9a32-611fd3c0c470.png">
    <img width="596" alt="스크린샷 2021-12-16 오후 4 22 45" src="https://user-images.githubusercontent.com/87518915/146782072-5b7a1d79-7c46-4018-9b46-904533576f9b.png">
    다음 그림을 보면 구성된 포트폴리오의 투자 비중, 2019년 1년을 투자했을 시에 1년간의 누적 수익률 변화 그래프를 볼 수 있다.

## Conclusion
*
## Reports
* Midterm : [report](https://github.com/Yunhee000/portfolio_composition/blob/main/report/2019102084_%E1%84%80%E1%85%B5%E1%86%B7%E1%84%8B%E1%85%B2%E1%86%AB%E1%84%92%E1%85%B4_%E1%84%8C%E1%85%AE%E1%86%BC%E1%84%80%E1%85%A1%E1%86%AB%E1%84%87%E1%85%A1%E1%86%AF%E1%84%91%E1%85%AD.pdf)
* Final : [report](https://github.com/Yunhee000/portfolio_composition/blob/main/report/2019102084_%E1%84%80%E1%85%B5%E1%86%B7%E1%84%8B%E1%85%B2%E1%86%AB%E1%84%92%E1%85%B4_%E1%84%8E%E1%85%AC%E1%84%8C%E1%85%A9%E1%86%BC%E1%84%87%E1%85%A1%E1%86%AF%E1%84%91%E1%85%AD.pdf)
