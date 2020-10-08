
- 4학년 1학기_텍스트마이닝을 이용한 소비자분석 과제  

  - study01= csv파일에서 인구수 그래프 시각화

  - study02=텍스트 데이터 빈도수 추출, wordcloud 생성  
    


-----------------------------------------------------------


## 프로젝트 주제 
<img src="https://user-images.githubusercontent.com/57060127/94516611-232a7380-0261-11eb-9f3d-0c5fbbd7b6fe.JPG" width=50%>

(자세한 설명: [최종발표자료](https://github.com/Jimin980921/Text_mining/blob/master/%ED%85%8D%EC%8A%A4%ED%8A%B8%20%EB%A7%88%EC%9D%B4%EB%8B%9D%20%EC%B5%9C%EC%A2%85%EB%B0%9C%ED%91%9C.pdf) 참고)
<br>
<br>


----------------------------------------------------------

## 개발 단계   
__1단계__: 네이버쇼핑 리뷰 크롤링(에어팟종류, 카테고리, 리뷰, 별점)  
  - [네이버쇼핑 리뷰 크롤링](https://github.com/Jimin980921/Text_mining/blob/master/Project/data/output.csv)
<img src="https://user-images.githubusercontent.com/57060127/89911794-cc26fb80-dc2c-11ea-937e-35dc4dcb099a.JPG" width=70%>
<br>
<br>

__2단계__: 수집한 데이터 전처리, 형태소 분석(토큰화)  
  - [토큰화](https://github.com/Jimin980921/Text_mining/blob/master/Project/data/token_output.csv)
<img src="https://user-images.githubusercontent.com/57060127/89912655-c1b93180-dc2d-11ea-9fce-180214872332.JPG" width=90%>
<br>
<br>


__3단계__: 긍정리뷰에서 빈도수 높은 단어 => positive 감정사전, 부정리뷰에서 빈도수 높은 단어 => negative 감정사전 추가  
<img src="https://user-images.githubusercontent.com/57060127/85818881-d2603600-b7ac-11ea-89fe-a3ee3220bbaa.png" width=70%>
<br>
<br>


__4단계__: 감정분석으로 각 리뷰의 긍정도 계산  
<br>
<br>


__5단계__: 데이터 정제  
별점과 긍정도가 상이한 경우 리뷰 삭제  
<img src="https://user-images.githubusercontent.com/57060127/85818955-076c8880-b7ad-11ea-9ce8-60ebcd9cc878.png" width=20%>
<br>
<br>


-----------------------------------------------------------------------

## 데이터 분석 결과  
 __1. 대부분의 리뷰 별점 4~5점대 분포. 소비자들이 부정적인 리뷰를 잘 남기지 않는 경향이 있음__  
 <img src="https://user-images.githubusercontent.com/57060127/85818322-55808c80-b7ab-11ea-9131-c54188373a14.png" width=20%>
 <br>
 
 __2. 에어팟 1세대보다 2세대의 긍정도가 높음. 카테고리별 긍정도 또한 전체적으로 증가__  
 
 에어팟 종류별 긍정도  |  에어팟 종류별 카테고리 긍정도
:------------------------------------:|:-------------------------:
![](https://user-images.githubusercontent.com/57060127/85819556-fde42000-b7ae-11ea-9e78-b491f47f55b7.png)  |  ![](https://user-images.githubusercontent.com/57060127/85819171-d476c480-b7ad-11ea-9a4c-092396b1306c.png)
<br>

__3. 성능이 변한 카테고리의 평균 긍정도가 성능 변화없는 카테고리의 평균 긍정도보다 3.5배 높음__    
하지만 성능이 변화없는 카테고리 또한 소폭 증가하였으므로 보유효과 또한 작용했다고 볼 수 있음  
<p>
<img src="https://user-images.githubusercontent.com/57060127/85820040-59fb7400-b7b0-11ea-91fa-7b2615f58778.png" width=50%>
</p>
<br>
<br>
<br>
 

- 유사 프로젝트  
   - [네이버 지도 크롤링 ](https://github.com/Jimin980921/Dongjak_bigdata_project) 
   - [유튜브 크롤링](https://github.com/Jimin980921/youtube_crawling)


