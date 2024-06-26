# 한 발 앞선 생각 - Don Touch

<img src="https://github.com/PDA-Dontouch/.github/assets/102455571/1f7ab842-5df8-4596-902d-6e378c64b536" style="height: 100px">
<img src="https://github.com/PDA-Dontouch/.github/assets/102455571/989bbaf4-15d7-4e5f-b937-fcde50714a2d" style="height: 100px">

<br/>

> 신한투자증권 프로 디지털 아카데미 3기 최종 프로젝트
> <br/><br/>
> 주제: 개인화된 금융 서비스를 제공하기 위한 클라우드 MSA 환경 구축 및 서비스 개발
> <br/><br/>
> 2024.05.29 ~ 2024.06.26 (6명)

<br/>
<br/>

## Team. DonTouch
| 이한슬 | 박유진 | 신의진 |
|:----:|:----:|:-----:|
|<img src = "https://avatars.githubusercontent.com/eehanseul" width=150px>|<img src = "https://avatars.githubusercontent.com/yjp8842" width=150px>|<img src = "https://avatars.githubusercontent.com/Tomk2d" width=150px>|
|[@eehanseul](https://github.com/eehanseul) <br/> PM |[@yjp8842](https://github.com/yjp8842) <br/> FE Tech Leader |[@Tomk2d](https://github.com/Tomk2d)  <br/> BE Tech Leader|
| 🔑 로그인 | 🫵 프론트 잘 이끌기 | 👊 백 잘 이끌기 |

| 허상진 | 박진언 | 이승택 |
|:----:|:----:|:----:|
|<img src = "https://avatars.githubusercontent.com/bookeers" width=150px>|<img src = "https://avatars.githubusercontent.com/parkjineon" width=150px>|<img src = "https://avatars.githubusercontent.com/seungtoctoc" width=150px>|
[@bookeers](https://github.com/bookeers)<br/> PL |[@parkjineon](https://github.com/parkjineon)|[@seungtoctoc](https://github.com/seungtoctoc)|
| ⚒️ P2P 데이터 수집, 가공 | 📅 달력 화면 | 🤝 배당주 조합 추천 |

<br/>

# 서비스 소개
<br />
금융투자협회 등 공신력 있는 기관의 통계에 따르면 주식 거래 활동 계좌 수 및 투자자 예탁금이 계속해서 증가하는 추세를 보이고 있습니다.
그 중 노후 준비를 위한 투자의 비중이 늘어나고 있고, 중/장년층은 정기적인 소득을 얻을 수 있는 '배당주 투자'에 관심을 두고 있습니다. 
50대 이상 투자자들이 개인 투자자들에게 지급된 배당금의 74% 이상을 받아가는 등, 배당주에 대한 수요는 폭발적으로 증가하는 중임을 볼 수 있습니다.

하지만, 이렇게 증가하는 수요에 대비해서 배당주 투자와 관련된 정보는 많이 없고 관련된 서비스도 부족합니다.
대부분의 정보는 보편적인 월배당 포트폴리오의 공유에 그치고, 개인의 재정상황과 투자 성향등을 고려하지 못합니다.
소수의 증권사들에서 배당주 관련 서비스가 출시되어 있기는 하나, 치명적인 단점들을 여럿 가지고 있습니다.

* 월당 1개의 종목만 고를 수 있고,
* 종목과 구매 주수를 직접 결정해야 하고,
* 예상 배당금을 볼 수 없으며,
* **개인화된 추천을 제공하지 못한다**는 단점을 가지고 있습니다.

<br />

그래서 저희는 이러한 문제점들을 해결하기 위한 서비스를 기획하였습니다.

* 투자성향과 보유한 주식 등을 통해 사용자 성향에 맞는 종목으로 **개인화된** 조합을 구성하고,
* 예상 배당금을 미리 확인할 수 있게 하여 일정한 월 소득을 설계하고,
* 소액 투자 및 포트폴리오를 분산할 수 있는 대안을 제시하고자 하였습니다.

# Project Architecture 
![image](https://github.com/PDA-Dontouch/.github/assets/128025654/4f1d5e14-5bc1-40e8-ad3a-2c17bbd851b0)

# Tech Stacks

# ERD

MSA 환경 구축을 위해 서비스의 단위별로 DB를 분리하였습니다.

<img width="595" alt="user" src="https://github.com/PDA-Dontouch/.github/assets/128025654/78e08049-a483-4b75-8fb5-ae8fc40e2beb">
<img width="821" alt="stock" src="https://github.com/PDA-Dontouch/.github/assets/128025654/d3378834-aabb-45d2-93ef-d5ef7c8f067c">
<img width="526" alt="order" src="https://github.com/PDA-Dontouch/.github/assets/128025654/942bcd2f-8e37-4711-9dc3-c20b39dc8e5f">
<img width="553" alt="estate" src="https://github.com/PDA-Dontouch/.github/assets/128025654/f603ca4a-3aec-49be-a028-b57d5419f646">
<img width="457" alt="energy" src="https://github.com/PDA-Dontouch/.github/assets/128025654/90de9cd7-3e52-436b-aaf7-3d2df4ffab4f">

# Algorithm
기업의 가치를 평가하기 위해 여러개의 재무제표를 활용하였습니다.
'안정', '성장', '배당' 3개의 영역으로 나누어, 아래와 같은 지표를 통해 종목 평가를 진행하였습니다.
![image](https://github.com/PDA-Dontouch/.github/assets/128025654/d1952695-39ef-4b44-b2ac-0dc1e92f66ae)
<br />
각각의 영역에 대한 점수를 매긴 후, Z점수 [(자료 값-평균)/표준편차] 를 활용하여 표준화하였습니다.

이렇게 계산된 종목의 평가 점수를 사용자의 투자 성향 및 보유한 주식에 따라 개인화 점수로 다시 계산합니다.
이후 사용자에게 최적이며, 매달 정기적인 배당을 받을 수 있는 조합을 추천해 줍니다. 


# Main Features

### 배당주 조합 추천 및 구매

사용자의 투자성향 및 투자 금액을 수집 후, 개인화된 배당주 조합을 추천해줍니다.
조합에 더 추가하고 싶은 종목이 있다거나 마음에 들지 않는 종목이 있다면 자유롭게 커스터마이징이 가능합니다. 
매 달의 배당주 조합을 고르고 나면 최종 조합 결과가 출력되며, 최대한 균등하게 배당을 수령할 수 있도록 배당금의 금액 맞춰 종목 수를 자동적으로 조절해줍니다.

### 개별 종목 추가 구매

조합 추천 이외에 추가적으로 개별 구매하고자 하는 종목이 있다면 검색을 통해 구매할 수 있습니다.
개별 종목의 상세 페이지에서는 실시간 가격과 원하는 기간(장/단기) 차트 및 재무제표를 보여주며, 사용자가 종목의 구매 여부를 판단하기 위한 많은 근거를 제공합니다.

### P2P 금융 상품 구매

소액 투자자 및 배당주보다 높은 수익을 원하는 투자자들을 위한 투자 상품 또한 구매할 수 있습니다.
사용자의 성향에 따라 수익률 혹은 안정성 순서대로 정렬하여 종목을 보여주며, 실제 규제에 따라 한 종목은 500만원 / 모든 P2P 상품은 합쳐서 4000만원까지 투자할 수 있도록 하였습니다.

### 메인 페이지 및 캘린더를 통한 배당 일정 확인

메인 페이지에서는 사용자의 투자성향, 이번달의 배당금과 배당 일정 및 총 자산을 볼 수 있습니다.

캘린더 페이지에서는 한달간의 배당 일정을 모두 볼 수 있으며 메인 페이지에서는 이번주의 일정으로 간소화하여 나타내었습니다.
배당금이 지급될 예정인 날짜와 종목명, 배당금을 한눈에 확인할 수 있도록 하여 사용자가 다양한 상품을 투자할 때 느꼈던 배당 일정 관리의 불편함을 해소시켰습니다.

관심종목 보기와 투자성향 다시 테스트하기 기능도 포함하여 최적의 개인화를 제공할 수 있도록 하였습니다.

<br />


# Project Structure

Frontend:
```
├─api
├─assets
│  ├─chart
│  └─footer
├─components
│  ├─Calendar
│  ├─Chatbot
│  ├─common
│  │  ├─Modal
│  │  ├─Product
│  │  │  └─Detail
│  │  └─Stock
│  ├─Energy
│  ├─Estates
│  ├─Login
│  ├─Main
│  ├─Skeleton
│  ├─Stock
│  │  ├─individual
│  │  └─trading
│  └─StockTest
├─hooks
├─pages
│  ├─Energy
│  ├─Estates
│  ├─Login
│  ├─Main
│  └─Stock
├─store
│  ├─reducers
│  │  ├─auth
│  │  ├─energy
│  │  ├─estates
│  │  └─stocks
│  └─webSocket
├─types
└─utils
```

Backend:
```

├─energy-server
│      └─src
│      ├─main
│      │  ├─java
│      │  │  └─donTouch
│      │  │      └─energy_server
│      │  │          ├─energy
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          ├─kafka
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          └─utils
│      │  └─resources
│      └─test
│          └─java
│              └─donTouch
│                  └─energy_server
├─estate-server
│      └─src
│      ├─main
│      │  ├─java
│      │  │  └─donTouch
│      │  │      └─estate_server
│      │  │          ├─estate
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  ├─service
│      │  │          │  └─utils
│      │  │          ├─kafka
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          └─utils
│      │  └─resources
│      └─test
│          └─java
│              └─donTouch
│                  └─estate_server
├─order-server
│      └─src
│      ├─main
│      │  ├─java
│      │  │  └─donTouch
│      │  │      └─order_server
│      │  │          ├─bankAccount
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          ├─holding
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          ├─kafka
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          ├─log
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          └─utils
│      │  └─resources
│      └─test
│          └─java
│              └─donTouch
│                  └─order_server
├─src
│  ├─main
│  │  └─java
│  │      └─donTouch
│  │          └─backend_server
│  └─test
│      └─java
│          └─donTouch
│              └─backend_server
├─stock-server
│  └─src
│      ├─main
│      │  ├─java
│      │  │  └─donTouch
│      │  │      └─stock_server
│      │  │          ├─dividend
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          ├─kafka
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          ├─krStock
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          ├─stock
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          ├─usStock
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          └─web
│      │  │              └─dto
│      │  └─resources
│      └─test
│          └─java
│              └─donTouch
│                  └─stock_server
├─user-server
│  └─src
│      ├─main
│      │  ├─java
│      │  │  └─donTouch
│      │  │      └─user_server
│      │  │          ├─kafka
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          ├─like
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          ├─oauth
│      │  │          │  ├─config
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          ├─user
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  ├─service
│      │  │          │  └─utils
│      │  │          ├─userEnergy
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          ├─userEstate
│      │  │          │  ├─domain
│      │  │          │  ├─dto
│      │  │          │  └─service
│      │  │          └─userStock
│      │  │              ├─domain
│      │  │              ├─dto
│      │  │              └─service
│      │  └─resources
│      └─test
│          └─java
│              └─donTouch
│                  └─user_server

```
