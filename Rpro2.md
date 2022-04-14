Warning and Error Code
--
* NaN
> 값이 계산 될 수 없을때

* '+'
> 명령어를 끝맺지 않았을 때

데이터의 형태
--
* 숫자형 (numerix)
>c(1,2,3)
* 문자형 (character)
> ""로 표시
> >k=c("a","b","c")

* 논리형 (logical)
>참과 거짓 //true=1, false=0<br>
>>논리형 사용<br>
>score > 90 // 90이상인가?<br>
> * TRUE TRUE FALSE TURE //console
****
>>인수형 조건을 달때 : [ ]<br>
 > * w <- score1[socore1 > 90]<br> #90이상 인수를 출력 
 <br> 96 96 //console
 > * y[1]<br> #y변수의 첫번째 인수 출력
 
데이터의 형태 변환
--
as.데이터형태()
>* as.character()<br>
>> 문자형으로 바꾸기 <br>
" " 형태로 변환
>* as.logical()
>> 숫자형 데이터가 0인지 아닌지를 체크
>* as.numberic()
>> "1"과 같은 형태 숫자형 변환
>* as.vector()
>> 벡터 형태
>* as.matrix()
>> 행렬형태
>* as.data.frame()
>> 변수이름과 인수 ID 추가
>* as.factor()
>> 범주형 변수

올림, 내림
--
* ceiling()
  > 
* floor()
  > 
* trunc()
  > 정수형으로 기록, 소수 버림
* round()
  > 반올림<br>
  > * round(변수,)

기초 통계랑
--
length()
> 표본의 크기 // 인수가 몇개인지

attach()
> 변수 이름 확인

dim()
> 표본의 크기, 변수 갯수

sum()
> 인수의 총 합

mean()
> 인수의 평균

median()
> 중앙값

max() | min()
> 최댓값, 최소값

range()
> 범위 (min,max)

var()
> 분산 | variance

sd()
> 표준편차 | standard deviation

rank()
> 순위 

summary()
> 최솟값, 제1사분위수, 중앙값, 평균, 제3사분위수, 최댓값 출력

두 개 이상의 변수 기초통계량
--
변수$변수 데이터
> class$dataset_name
> * mean(class$dataset_name)

apply 통계량
--
##### 데이터에 임의의 함수를 적용하여 결과를 얻는다. <br> 조건문보다 속도가 빠르고, 짧은 코드로 반복 연산이 가능하다. <br> 

apply(데이터셋,적용방향,그룹함수)
> + dataset : array형식 | matrix등<br>
> + margin : 1 = 행,  2 = 열
> + fun : 반복적 적용 함수<br>
> + ... : fun에서 추가적인 인수
> >  x <- matrix(1:20,4,5)<br>
//1-20까지 행4, 열5 
> > + ex) apply(X=x,margin=1,FUN=max)<br>// 각 행에서 최댓값<br>
> + 행 별로 합 계산
> > apply(dataset,1,sum) <br>
> > = rowSums(dataset) 
> + 열 별로 합 계산
> > apply(dataset,2,sum) <br>
> > = colSums(dataset) 
> + 행 별로 평균 계산
> > apply(dataset,1,mean) <br>
> > = rowMeans(dataset) 


>
> > + 응용 : 변동계수 구하기 [표준편차 / 산술평균]<br>
> > 1. sd(dataset $ data2) / mean(dataset $ data2)
> > 2. apply(dataset,2,)funtion(x) sd(x)/mean(x)<br>
>
> >  결측치 제거하기 : funtion(dataset,na.rm = T)<br>
> > na.rm | NA remove


aggregate() #요인별 함수
--
aggregate(dataset,by,Function,...)
>* dataset
>* by : list(범주)<br>
> // dataset의 범주<br>
> 여러 범주 선택하고 싶으면 (list1 , list2)
>* function

열의 이름 바꾸기
> names()=c("list1","list2","funtion output")