# 텍스트 마이닝을 이용한 소비자 심리분석 프로젝트  
(자세한 설명: [최종발표자료](https://github.com/Jimin980921/Text_mining/blob/master/%ED%85%8D%EC%8A%A4%ED%8A%B8%20%EB%A7%88%EC%9D%B4%EB%8B%9D%20%EC%B5%9C%EC%A2%85%EB%B0%9C%ED%91%9C.pdf) 참고)

## 주제  
전자제품의 경우 주기적으로 리뉴얼하여 새로운 제품을 판매하는 경향이 있음  
__소비자는 향상된 성능을 체감하는지, 아니면 단순히 비싼 신제품을 소유했다는 보유효과를 느끼는지__ 에대한 소비자심리에대한 연구 
<br>

__데이터__: 네이버 쇼핑 리뷰  
> '리뷰'란 제품에 만족한 이유를 드러내는 비정형 데이터. 소비자의 솔직하고, 의도되지 않은 데이터라는 장점이 있음
<br>

----------------------------------------------------------

## 개발 단계   
### 1단계: 데이터 수집  
> 네이버쇼핑 리뷰 크롤링(에어팟종류, 카테고리, 리뷰, 별점)  
  - __네이버쇼핑 리뷰 크롤링__ - [data](https://github.com/Jimin980921/Text_mining/blob/master/Project/data/output.csv)
<img src="https://user-images.githubusercontent.com/57060127/89911794-cc26fb80-dc2c-11ea-937e-35dc4dcb099a.JPG" width=70%>
<br>
<br>

### 2단계: 데이터 전처리  
> 불용어 제거, 형태소 분석(토큰화)  
  - __토큰화__ - [data](https://github.com/Jimin980921/Text_mining/blob/master/Project/data/token_output.csv)
<img src="https://user-images.githubusercontent.com/57060127/89912655-c1b93180-dc2d-11ea-9fce-180214872332.JPG" width=90%>
<br>
<br>


### 3단계: 감정사전 추가   
> 긍정리뷰에서 빈도수 높은 단어 => positive 감정사전 / 부정리뷰에서 빈도수 높은 단어 => negative 감정사전 추가  
<img src="https://user-images.githubusercontent.com/57060127/85818881-d2603600-b7ac-11ea-89fe-a3ee3220bbaa.png" width=70%>
<br>
<br>


### 4단계: 리뷰 긍정도 계산  
> 긍,부정단어를 추가한 감정사전을 이용하여 리뷰 긍정도 계산 (범위 0~1, 1에 가까울수록 긍정, 0에 가까울수록 부정)  
<br>
<br>


### 5단계: 데이터 정제  
> 별점은 높지만, 리뷰 긍정도가 낮게 측정된 경우 해당 리뷰는 분석에서 제외함  
> 예) '너무 좋아요! 걱정헀는데 다행입니다', 별점:5점 / 리뷰긍정도: 0.1 => 삭제  
<img src="https://user-images.githubusercontent.com/57060127/85818955-076c8880-b7ad-11ea-9ce8-60ebcd9cc878.png" width=20%>
<br>
<br>
 

-----------------------------------------------------------------------

## 데이터 분석 결과  
 __1. 대부분의 리뷰 별점 4~5점대 분포. 소비자들이 부정적인 리뷰를 잘 남기지 않는 경향이 있음__  
 <img src="https://user-images.githubusercontent.com/57060127/85818322-55808c80-b7ab-11ea-9131-c54188373a14.png" width=20%>
 <br>
 __2. 에어팟 1세대, 2세대 모두 '음질'에 대한 리뷰가 많음. 소비자가 에어팟에서 음질에 가장 관심이 있음을 알 수 있음__  
 <img src="https://user-images.githubusercontent.com/57060127/102316162-c82f2f80-3fb8-11eb-83b7-8b8fe2c7f05b.JPG" width=20%>  
 <br>
 
  
 __3. 에어팟 1세대보다 2세대의 긍정도가 높음. 카테고리별 긍정도 또한 전체적으로 증가__  
 > 예) 기능 0.89->0.93 , 배터리수명 0.87->0.96  
 
 에어팟 종류별 긍정도  |  에어팟 종류별 카테고리 긍정도
:------------------------------------:|:-------------------------:
![](https://user-images.githubusercontent.com/57060127/85819556-fde42000-b7ae-11ea-9e78-b491f47f55b7.png)  |  ![](https://user-images.githubusercontent.com/57060127/85819171-d476c480-b7ad-11ea-9a4c-092396b1306c.png)
<br>

__4. 성능이 변한 카테고리의 평균 긍정도가 성능 변화없는 카테고리의 평균 긍정도보다 3.5배 높음__    
> 하지만 성능이 변화없는 카테고리 또한 소폭 증가하였으므로 보유효과 또한 작용했다고 볼 수 있음  
<p>
<img src="https://user-images.githubusercontent.com/57060127/85820040-59fb7400-b7b0-11ea-91fa-7b2615f58778.png" width=50%>
</p>
<br>
<br>
<br>
 

- 유사 프로젝트  
   - [네이버 지도 크롤링 ](https://github.com/Jimin980921/Dongjak_bigdata_project) 
   - [유튜브 크롤링](https://github.com/Jimin980921/youtube_crawling)
<br>
<br>


------------------------------------------------------------------------------

- 4학년 1학기_텍스트마이닝을 이용한 소비자분석 과제   
 
  - study01  
   > csv파일에서 인구수 데이터 가져와서 시각화 하기  
   <img src="https://user-images.githubusercontent.com/57060127/102313968-ef83fd80-3fb4-11eb-805c-539e6baf4241.JPG" width=40%>  
   
  - study02  
  > 텍스트 데이터 빈도수 추출, wordcloud 생성     
