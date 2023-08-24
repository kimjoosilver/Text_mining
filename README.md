# Text_mining

# 반려인을 위한 숙소 리뷰 분류 모델

### 김주은, 황민규

![데이터마이닝_팀_프로젝트_1조_page-0002](https://github.com/kimjoosilver/Text_mining/assets/87303227/035179b8-b79e-4530-8225-4c23db9221f3)
![데이터마이닝_팀_프로젝트_1조_page-0003](https://github.com/kimjoosilver/Text_mining/assets/87303227/d8022d02-3e43-4903-9b39-b5096dca1d4e)
![데이터마이닝_팀_프로젝트_1조_page-0004](https://github.com/kimjoosilver/Text_mining/assets/87303227/d6f1bad3-fb8c-4363-975f-cd9c270a4a39)
![데이터마이닝_팀_프로젝트_1조_page-0005](https://github.com/kimjoosilver/Text_mining/assets/87303227/cd548ba2-d52b-4993-97eb-c1c054777718)

농림축산식품부에 따르면 22년 기준 국내 반려동물 양육가구는 602만 가구로 10년 전보다 65%이상 증가했다. 이에 따라 반려동물 관련 시장의 규모도 커지고 있습니다. 

KB 경영연구소에 따르면 반려인의 20.4%이 향후 반려동물 여행/액티비티 관련 앱의 사용을 희망하고 있으며 네이버 검색이 트렌드에서도 '애견동반 숙소' 키워드가 우상향 하는 것으로 애견동반 숙소에 대한 수요가 꾸준히 증가하고 있음을 확인했습니다.

![데이터마이닝_팀_프로젝트_1조_page-0006](https://github.com/kimjoosilver/Text_mining/assets/87303227/bf448c34-f7fc-4650-848c-39d742ffb786)

이에 저희 조는 여론조사 전문기관 리얼미터의 숙박앱 브랜드 선호도 상위에 있는 어플리케이션을 직접 사용해 보았습니다.

숙박업체 어플들에서 반려동물 동반 가능한 숙소 유무를 구별할 수 있는 버튼을 쉽게 찾을 수 있었습니다. 하지만 숙소 후기에는 반려동물 동반 유무와 관계없이 섞여있어 해당 숙소가 반려동물 동반에 좋을 숙소인지는 알기 어려웠습니다.

'해당 숙소가 반려동물을 동반할 때 좋은 숙소일까?'의 정보를 제공하기 위해 '반려인을 위한 숙소 리뷰 분류 모델'을 다음과 같이 만들었습니다.

반려동물 동반 가능 숙소를 대상으로 

1. 반려동물 동반 유무 모델 (키워드 토큰 유무를 기준으로 분류)

2. 반려동물 동반 유저의 댓글에서 긍부정 분류 모델

   
해당 모델을 만들기 위해 데이터는 야놀자, 여기어때, 에어비앤비 3개의 도메인에서 총 42,353개의 데이터를 크롤링하여 수집하였습니다.

![데이터마이닝_팀_프로젝트_1조_page-0007](https://github.com/kimjoosilver/Text_mining/assets/87303227/9edcf146-4987-4d91-9214-fe945ba40e02)

![데이터마이닝_팀_프로젝트_1조_page-0010](https://github.com/kimjoosilver/Text_mining/assets/87303227/45b9f4f0-b141-4ce7-8b60-0905f9d7d737)
![데이터마이닝_팀_프로젝트_1조_page-0011](https://github.com/kimjoosilver/Text_mining/assets/87303227/c01dfdf2-b850-48ce-9b2d-7c2eeeee0a11)

![데이터마이닝_팀_프로젝트_1조_page-0008](https://github.com/kimjoosilver/Text_mining/assets/87303227/4901e36c-3b82-47de-8cb4-cfb26de96467)
총 42,353개의 데이터를 수집하였지만 데이터 전처리 후 5,000여개의 데이터만 남았습니다. 

데이터의 수가 예상했던 것보다 훨씬 적어 당황했지만 시간적 한계로 5,000여개의 데이터만을 이용하여 분석 및 모델링을 진행하게 되었습니다.

긍부정 분류 모델을 만들기 위해서는 라벨이 필요하기 때문에 다음과 같은 기준으로 모든 데이터에 부정/혼합/긍정 라벨링을 하였습니다.

![데이터마이닝_팀_프로젝트_1조_page-0009](https://github.com/kimjoosilver/Text_mining/assets/87303227/bd7e3f07-16a2-4d97-84a5-922045fba205)

라벨의 정확도를 위해 라벨링은 불용어 처리 전 원본 댓글을 읽으며 라벨링 하였습니다.

![데이터마이닝_팀_프로젝트_1조_page-0012](https://github.com/kimjoosilver/Text_mining/assets/87303227/0e87a73d-59ae-492e-abac-641c31a0e46e)

![데이터마이닝_팀_프로젝트_1조_page-0013](https://github.com/kimjoosilver/Text_mining/assets/87303227/19a72ba7-fdb1-47b4-ac10-c4ee5d18b2e0)

![데이터마이닝_팀_프로젝트_1조_page-0014](https://github.com/kimjoosilver/Text_mining/assets/87303227/9177177b-e6b3-4e55-aab3-c5a7eb7943ee)
