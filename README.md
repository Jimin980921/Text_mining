
# 4학년 1학기_텍스트마이닝을 이용한 소비자분석 과제

study01= csv파일에서 인구수 그래프 시각화

study02=텍스트 데이터 빈도수 추출, wordcloud 생성


-----------------------------------------------------------


# 팀프로젝트 
* 전자제품의 경우, 일정기간마다 리뉴얼하여 제품을 출시한다. 
본 프로젝트에서는 '에어팟 1세대와 2세대의 성능차이를 소비자가 실제로 느끼는가? 성능의 변화는 느끼지 못하고 보유효과,심적회계원리의 영향을 받는것인가?'를 알아보고자 하였다.

(자세한 설명: 프로젝트 계획서, 최종발표자료 참고)

* 네이버쇼핑 리뷰 크롤링(에어팟종류, 카테고리, 리뷰, 별점) > 수집한 데이터 전처리, 형태소 분석, 빈도수 분석 > 긍정리뷰에서 빈도수 높은 단어 positive 감정사전에 추가, 부정리뷰에서 빈도수 높은 단어 negative 감정사전에 추가 > 감정분석으로 각 리뷰의 긍정도 계산 > 별점과 긍정도가 상이한 경우 리뷰 삭제 > 에어팟 종류별 카테고리 긍정도 변화 분석


* 결과: 
 1. 대부분의 리뷰 별점 4~5점대 분포. 소비자들이 부정적인 리뷰를 잘 남기지 않는 경향이 있음.
 <img src="https://user-images.githubusercontent.com/57060127/85818322-55808c80-b7ab-11ea-9131-c54188373a14.png" width="70" height="150">
