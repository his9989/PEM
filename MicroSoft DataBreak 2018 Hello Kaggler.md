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

#### KDD Cup
1. KDD Cup이란?
  * 유명한 KDD 학회의 Competition. 
  * 2018년 KDD Cup은 6,000팀, 4,000소속, 49개국 참여
2. 내 전문 분야의 Competition에 도전하자.
3. 머신러닝의 Competitons을 위한 Best Practices
  * Feature Enginerring
    + model부터 구축하지 말고, 데이터 분석 먼저
  * Diverse Algorithms
    + 고정적인 알고리즘 사용하지 말고, 여러 가지 알고리즘을 "시도"
    + 생각치 못한 결과가 나올 수 있다.
  * Cross Validation
    + 가장 적합한 Validation을 적용하는게 중요.
  * Ensemble
    + 내가 시도한 모든 데이터를 조합
    + Validation에서 사용한 기법에 알맞는 stacking 방법으로 수행
  * Collaboration
    + 협업. 구성원들이 만들어낸 결과물을 취합하기 위해, Validation set을 어떻게 할 지 공유해야함.
  * Pipeline
    + 위의 과정들, (Feature Algorithms, Cross Validation, Ensemble) 등의 일련의 머신러닝 작업 과정을 makefile처럼 착착착 수행하도록 하는 과정

<hr>

## [Time3] : 대한민국 인맥지도
### 발표자 : 강규영 (박스앤위스커, 데이터 시각화)
### https://akngs.github.io/smallworld/

#### 관련 내용
1. 데이터 수집 : wiki Data 사이트 사용 + sparql
 * wiki data : 일반 대중이 데이터베이스를 수정.
 * https://www.wikidata.org/wiki/Wikidata:Main_Page
2. 주요 인물 찾기 : 파이썬 + NetworkX
 * https://networkx.github.io
 * 즉, 한 인물에 대하여 관계를 갖고 있는 인물 중 주요 인물을 찾는 알고리즘 구현
 * 관계를 추가하기 위해 노드가 추가될 때 마다 sorting을 통해, 최단거리 계산해서 허브 구함
 * 인간관계 데이터에서는 과하게 데이터가 길어질 것 같지 않지만, 다른 분야의 경우 느려질 수 있다.
3. 그래프 탐색기 (d3js)
 * https://d3js.org
 * 난제: 노드가 많아지면 그래프는 어떻게 그리는가?
   + 노드 간의 충돌을 방지하는 코드 구현
   + 밑의 코드처럼 노드 설정
4. 기타 유관 사이트
 * 깃헙 페이지스 : https://pages.github.com/
 * 지킬사이트 생성기 : https://jekyllrb.com/

<code>
 
 this.forceSim
  .force("center", d3.forceCenter(0,0))
  ...
  .force("colide", d3.forceCollide(30))
  
</code>
  
## [Time4] : QA에 사용되는 Knowledge Embedding 응용 및 활용 방안
### 발표자 : 최동근 (Saltlux, Hong.univ senior)

#### 관련 내용
1. Knowledge Base : 
  ex) "대한민국"의 "대통령"은 "문재인"이다.
  * 스키마를 구축하고 트리플을 쌓는다.
  * 
  
2. QA System
  * KBQA : 지식 베이스 기반 질의처리 모듈. 구조화가 용이한 도메인에 적합하다.
    + ex) 대한민국의 대통령은?
    + 위의 질문에 대해 feature 추출. 대한민국이 주어이고 대통령이 목적어 임을 추출
    + 질의문을 지식베이스에게 보내서 정답을 추출
    + 자연스러운 자연어 처리를 통해 정답 출력
  
  * IRQA : 검색 베이스 기반
  
  
