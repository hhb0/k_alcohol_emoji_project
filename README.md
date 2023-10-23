# k_alcohol_emoji
K-Trenditional Drinks
이모지로 보는 이 전통주 모지?

### `k_alcohol: 감성 요인에 따른 전통주 맞춤형 추천`을 업그레이드

[서비스 링크](https://k-trenditional-drinks.streamlit.app/)

## 1. 기획 의도
**1. 전통주 인식**  
원소주 출시에 따른 전통주 인지도가 상승하였으나 여전히 '소주', '막걸리'에 국한된 전통주에 대한 인식이 존재  
  
**2. 성장하는 시장**  
 SNS상 타 주종(맥주, 소주, 와인 등) 대비 낮은 인터랙션을 갖고있어 시장 성숙도를 기준으로 도입기로 판단   
   
**3. 기서비스 한계**  
당도, 신맛, 청량감, 도수 등 정량적인 요구 사항에 맞추어 술을 추천해 주는 서비스 존재. 그러나 기 서비스는‘슬플 때’, ‘특정 음식에 어울리는’, ‘친구들과 함께‘ 등정성적인 음주 상황 특성 배제 및 공유 심리를 자극하는 요소가 부족한 한계

## 2. 핵심 기능  
- 유저로부터 자신의 기분, 현재 상황 및 원하는 재료와 음식에 맞는 이모지 선택받아 이모지에 해당하는 키워드 임베딩  
- 수집한 전통주 데이터와 유저 입력값의 코사인 유사도를 비교하여 전통주를 추천  
- 전통주 소개 문구를 바탕으로 유저 입력값에 어울리는 추천 결과 안내 문구 생성

## 3. Service Flow
![service_flow](https://github.com/hhb0/k_alcohol_emoji_project/assets/131653682/0db6730a-e2f6-4593-b92d-eff0eb4e28c1)
  
## 4. 데이터셋 및 사용 기술
**데이터 수집 및 가공**
- 893건의 전통주 데이터 크롤링 (이름, 재료, 음식, 소개 등 텍스트 형태)

**사용 기술**
- Python
    - Beautiful Soup: 크롤링한 전통주 데이터 파싱
    - Pandas: 데이터 조작 및 분석
    - Openai Embedding API: 전통주 데이터와 유저 입력값을 임베딩
    - Openai GPT-3.5: 추천 결과 안내
