#### 18.10.07 캐글 뽀개기

<hr>

## [Time1] : 기업 현장에서의 데이터 과학
### 발표자 : 조동환 (SKT DT 추진단장)
### 발표자가 6년간 구축한 데이터사이언스 처리 과정 (사진 자료 有)
* 데이터 과학 = 기술 + 변형 적용 <br>
* 발표자가 새로운 데이터 관리 조직을 만들어서 6년간 구축한 결과
* 요즘 SK에서는 성과 평가는 없고, 피드백만 해준다.
* 아주 Extream한 outliers에 대한 관리만 해주고, 중간 조직원들에 대한 줄세우기는 없다.

#### 1. 조직 내부 데이터 
1-1. Internal Structured Data + Internal UnStructured Data + External Data Sources = Data lake <br>
  * Data Lake 관리는 Apache Hadoop, ORC, Apache Ranger, Kerberps 등
  * Data Lake 구축을 하는데 2년 걸림

2-1. Data Lake(데이터 모음)을 Fast Data Store(apache Spark) 프레임워크로 처리(Data marts) <br>
2-2. Data Lake, Data Store에 대해서 Self Serviced Data Services하고 결과를 Data Analysts <br>
2-3. Data Lake를 Feature Store + Machine Learning Engine(R, Python, TensorFlow 등 이용)으로 Data Analysts

3-1. 결과물에 대해 Subject Matter Experts, Internal Systems

#### 2. 조직 외부 데이터 : 발표자가 조직 외적으로 조직 구축을 위해 진행한 일
1. data governance : 데이터 통합 관리
2. Data와 IT의 충돌 조율 (삐지지마ㅏ) <br>
    * 실제 개발진과 데이터를 관리하는 조직, 즉, Data vs IT는 다툼이 좀 있다.
    * IT 입장과 데이터 관리 조직 입장 간의 데이터 분석에 의한 결과의 정확도 기대가 좀 다를 수 있다.
3. Data Privacy : 데이터 보안
4. Transformation Strategy <br>
    * Group Up Strategy : 시작부터 기반을 철저히 계산해서 구축
    * Small Wins Strategy : 조금씩의 성과를 보여줌으로서 발전
5. Company Culture : 기업 내부 문화 (직원들 R 수업)
6. Storong LeaderShip : 대표님의 지지
7. 뭐 기타 등등

<hr>

## [Time2] : Mastering Machine Learning with Competitions
### 발표자 : 이정윤 (MicroSoft 본사, OneML 대회 운영진)

#### 1. KDD Cup
1. KDD Cup이란?
  * 유명한 KDD 학회의 Competition. 
  * 2018년 KDD Cup은 6,000팀, 4,000소속, 49개국 참여
2. 

