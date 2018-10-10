# Heat_island - in Seoul
Analysis Heat_island in Seoul 

빅데이터 청년인재 프로젝트

 Heat_island

분석 개요:
주제: 	  서울시의 열섬 현상을 분석한다.

열섬현상 - 주변 도시보다 3~5도 이상 높을시 열섬현상으로 규정

	- 원인: 도시내부의 축적열 + 도시구조로 인한 더딘 냉각화 + 공기오염

사용 데이터 :  데이터 추출 기간:  2014-01-01 ~2017-12-31

	     1. 기상 : 서울시 기상청 데이터  aws.seoul.go.kr /  http://www.weather.go.kr
	     
 	     2. 도시 면적 : 공공데이터 포탈   Data.go.kr
	     
	     3. 대기오염: 서울시 대기오염   www.airkorea.or.kr

분석 : 사전작업

	서울시 온도 - 경기도 온도 >= 3℃  : 열섬이 일어난 것으로 간주 label = 1
	
	서울시 온도 - 경기도 온도 < 3℃  : 열섬이 일어나지 않은 것으로 간주 label = 0

	Season 값 부여 -> 계절에 따른 고정효과 분석	

분석 : EDA 

	Label 비중 분석 -> 열섬 현상 많이 일어나는 구 확인
	
	Pair plot :  상관관계 분석
	
	시계열 분석 :  열섬 시계열적 분포 확인, 

분석 : 분석 
       	Season Dummy variable - Data set.1
	
	Decompose	- Data set.2
	
	Data set1, set2 각 각 분석 툴 사용
	
	-Logistic Regression
	
	-ANN
	
	-Random Forest
	
	-SVM
	
	-XG boost
