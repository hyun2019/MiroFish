# MiroFish Manual

## 전체 파이프라인

MiroFish는 단순히 문서를 요약하는 도구가 아닙니다.  
사용자가 넣은 자료를 바탕으로 `가상의 사회 환경`을 만들고, 그 안에서 여러 에이전트가 반응하도록 돌려 본 다음, 그 결과를 보고서 형태로 정리하는 시스템입니다.

전체 흐름은 아래 5단계로 보면 됩니다.

### 1. 현실 자료 업로드

사용자는 먼저 PDF, TXT, MD 같은 문서를 올립니다.

예를 들면:

- 사건 보고서
- 뉴스 정리 문서
- 정책 초안
- 기업 분석 자료
- 소설이나 시나리오 초안

그리고 함께 이런 식의 요청을 입력합니다.

- "이 정책이 발표되면 여론이 어떻게 움직일까?"
- "이 사건 이후 온라인 반응은 어떻게 번질까?"
- "이 소설 인물들이 이후에 어떤 선택을 할까?"

즉, `문서`는 재료이고, `자연어 요청`은 시뮬레이션 목표입니다.

### 2. 문서에서 세계관 뼈대 추출

시스템은 업로드된 문서를 읽고, 그 안에서 중요한 등장 주체와 관계를 뽑아냅니다.

쉽게 말하면 이런 작업입니다.

- 누가 중요한 사람인지
- 어떤 조직이 등장하는지
- 누가 누구와 연결되어 있는지
- 어떤 갈등, 협력, 영향 관계가 있는지

이 단계의 결과는 `그래프`입니다.

여기서 그래프는:

- 노드: 사람, 조직, 집단, 기관 같은 주체
- 엣지: 주체들 사이의 관계

즉, 문서를 그냥 긴 텍스트로 두지 않고, `서로 연결된 구조`로 바꾸는 단계입니다.

### 3. 그래프를 바탕으로 에이전트 사회 구성

그래프가 만들어지면, 시스템은 그 안의 주체들을 시뮬레이션용 에이전트로 바꿉니다.

이때 각 에이전트는 대략 이런 정보를 갖게 됩니다.

- 어떤 성격과 입장을 가질지
- 어떤 배경과 기억을 가질지
- 누구와 더 가깝고 누구와 대립하는지
- 어떤 상황에서 적극적으로 반응할지

즉, 문서 속 인물과 조직을 `행동 가능한 디지털 행위자`로 바꾸는 단계입니다.

### 4. 가상 소셜 플랫폼에서 시뮬레이션 실행

준비된 에이전트들은 가상의 소셜 미디어 환경에서 서로 반응합니다.

이 프로젝트는 코드상으로 Twitter/Reddit 스타일의 환경을 사용합니다.

여기서 에이전트들은 예를 들어:

- 글을 올리고
- 다른 글에 반응하고
- 지지하거나 반대하고
- 확산시키거나 무시하고
- 시간이 지나면서 입장을 바꾸기도 합니다

중요한 점은, 이 단계가 정적인 분석이 아니라 `시간이 흐르는 상호작용 시뮬레이션`이라는 것입니다.

즉, "문서 내용이 이렇다"에서 끝나는 것이 아니라  
`그 상황이 실제로 굴러가면 다음에 무슨 일이 이어질까?`를 실험해 보는 단계입니다.

### 5. 결과 보고서 생성 및 상호작용

시뮬레이션이 끝나면 시스템은 결과를 바탕으로 보고서를 만듭니다.

이 보고서에는 보통 이런 내용이 들어갑니다.

- 어떤 세력이 어떻게 반응했는지
- 여론이 어떤 방향으로 움직였는지
- 갈등이 커졌는지 줄었는지
- 어떤 변수나 사건이 흐름을 바꿨는지
- 최종적으로 어떤 결과가 유력해 보이는지

그 다음에는 사용자가 더 깊게 들어갈 수 있습니다.

- 특정 에이전트와 대화
- 보고서에 대해 추가 질문
- 왜 이런 결과가 나왔는지 재질문

즉, 결과를 한 번 받고 끝나는 구조가 아니라 `시뮬레이션 세계를 계속 탐색`할 수 있게 되어 있습니다.

## 한 줄로 요약하면

MiroFish의 전체 파이프라인은 아래처럼 이해하면 됩니다.

`문서 업로드 -> 핵심 주체/관계 추출 -> 그래프 생성 -> 에이전트 사회 구성 -> 소셜 시뮬레이션 실행 -> 결과 보고서와 상호작용`

## 이 파이프라인의 핵심 의미

보통 LLM 앱은 문서를 읽고 바로 답변을 만듭니다.  
MiroFish는 그보다 한 단계를 더 갑니다.

문서를 읽은 뒤 곧바로 답하는 것이 아니라:

1. 문서에서 세계를 구조화하고
2. 그 세계 안에 행위자를 만들고
3. 행위자들이 서로 영향을 주고받게 돌려 본 뒤
4. 그 결과를 다시 분석합니다

그래서 이 프로젝트는 `요약기`나 `QA 챗봇`보다는 `예측용 시뮬레이션 엔진`에 더 가깝습니다.

## 그래프란 무엇인가

여기서 그래프는 차트나 그래프 이미지가 아니라 `관계도 데이터`입니다.

아주 단순하게 보면:

- 점(node): 사람, 조직, 집단, 기관 같은 주체
- 선(edge): 그 주체들 사이의 관계

예를 들면 이런 식입니다.

- `학생 A`
- `대학교 B`
- `언론사 C`

그리고 관계는:

- `학생 A -> 대학교 B` : 재학 중
- `언론사 C -> 사건 X` : 보도함
- `조직 D -> 학생 A` : 지지함

즉, 긴 문장을 그대로 들고 있는 대신,  
`누가 있고`, `누가 누구와 어떤 관계인지`를 구조화해서 저장한 것이 그래프입니다.

MiroFish에서는 이 그래프가 단순 저장용이 아니라,  
이후에 에이전트를 만들고 시뮬레이션을 돌리기 위한 `세계의 뼈대` 역할을 합니다.

## 문서에서 그래프로 어떻게 바꾸는가

핵심 원리는 아래 3단계입니다.

### 1. 문서를 먼저 텍스트로 바꾼다

업로드된 PDF, MD, TXT 파일에서 먼저 순수 텍스트를 추출합니다.

이 단계에서는:

- PDF면 페이지별 텍스트 추출
- TXT/MD면 인코딩을 맞춰 읽기
- 줄바꿈과 공백을 정리

를 수행합니다.

즉, 첫 단계는 `문서를 읽을 수 있는 텍스트 형태로 만드는 작업`입니다.

### 2. 어떤 종류의 주체와 관계를 볼지 먼저 정한다

문서에서 바로 모든 인물을 마구 뽑는 것이 아니라,  
먼저 LLM이 문서와 사용자의 요청을 보고 `이번 문서에서 중요한 엔티티 타입과 관계 타입`을 정의합니다.

예를 들면 이런 식입니다.

- 엔티티 타입:
  - `Student`
  - `Professor`
  - `University`
  - `MediaOutlet`
  - `Person`
  - `Organization`

- 관계 타입:
  - `STUDIES_AT`
  - `WORKS_FOR`
  - `REPORTS_ON`
  - `SUPPORTS`
  - `OPPOSES`

즉, 시스템은 먼저  
`이 문서에서는 어떤 종류의 사람/조직/관계를 중심으로 세계를 볼 것인가`를 정합니다.

이 단계를 코드에서는 보통 `ontology` 생성이라고 부릅니다.

### 3. 텍스트를 잘게 나눠 그래프 엔진에 넣는다

그 다음 전체 문서를 한 번에 처리하지 않고 작은 조각으로 나눕니다.

이유는:

- 문서가 길 수 있고
- 한 번에 처리하면 누락이 생길 수 있고
- 부분별로 관계를 더 안정적으로 뽑기 위해서입니다

이렇게 나눈 텍스트 조각들을, 앞에서 만든 엔티티/관계 정의와 함께 그래프 엔진에 넣습니다.  
그러면 엔진이 각 조각에서:

- 어떤 주체가 등장하는지
- 그 주체가 어떤 타입인지
- 어떤 관계가 문맥상 성립하는지

를 읽어서 노드와 엣지로 축적합니다.

즉, 한 줄 요약하면:

`문서 텍스트 추출 -> 중요한 타입 정의 -> 텍스트를 조각내어 관계 추출 -> 그래프에 누적`

## 핵심 인물/조직/관계를 추출하는 방식

이 프로젝트는 전통적인 규칙 기반 추출기보다는,  
`LLM + 그래프 엔진` 조합으로 추출한다고 이해하는 편이 맞습니다.

쉽게 풀면 방식은 이렇습니다.

### 1. 먼저 "무엇을 중요한 주체로 볼지" 범주를 만든다

문서마다 중요한 주체는 다릅니다.

- 대학 이슈면 학생, 교수, 학교, 언론이 중요할 수 있고
- 기업 이슈면 CEO, 직원, 회사, 규제기관이 중요할 수 있습니다

그래서 MiroFish는 문서와 시뮬레이션 요청을 보고  
`이번 문서에 맞는 주체 범주`를 먼저 만듭니다.

이게 있어야 추출이 덜 엉뚱해집니다.

### 2. 텍스트 문맥 안에서 실제 등장 대상을 찾는다

그 다음 각 텍스트 조각을 읽으면서:

- 실제로 등장하는 사람/조직/집단이 무엇인지
- 그들이 어떤 범주에 속하는지
- 요약하면 어떤 성격의 주체인지

를 판단합니다.

즉, 단순 키워드 매칭이라기보다  
`문맥을 보고 이 표현이 누구를 가리키는지`를 해석하는 방식에 가깝습니다.

### 3. 주체들 사이의 연결을 관계로 만든다

예를 들어 문장 안에 이런 정보가 있으면:

- 누구는 어디 소속이다
- 누구는 누구를 비판했다
- 어떤 기관이 어떤 사안을 발표했다
- 어떤 매체가 어떤 사건을 보도했다

이런 연결을 관계로 바꿉니다.

즉:

- 소속 관계
- 지지/반대 관계
- 보도 관계
- 반응 관계
- 협력/대립 관계

같은 것들을 엣지로 저장합니다.

### 4. 여러 문서 조각에서 나온 결과를 합쳐 하나의 관계도로 만든다

한 인물이나 조직은 문서 여러 부분에 반복 등장할 수 있습니다.  
시스템은 이런 정보를 모아서 최종적으로 하나의 그래프로 정리합니다.

그래서 결과물은 단일 문장이 아니라  
`전체 문서에서 반복적으로 드러난 사회적 연결 구조`가 됩니다.

## 아주 짧게 정리하면

그래프는 `문서를 사람/조직/관계 중심의 구조로 바꾼 것`입니다.

구축 원리는:

1. 문서를 텍스트로 추출하고
2. LLM이 중요한 엔티티 타입과 관계 타입을 정한 뒤
3. 텍스트를 잘게 나눠
4. 각 조각에서 인물/조직/관계를 읽어
5. 전체 관계도로 합치는 방식입니다.

## 그래프가 이후 시뮬레이션으로 어떻게 이어지는가

그래프는 중간 산출물일 뿐이고, MiroFish의 목적은 그래프 자체를 보는 데 있지 않습니다.  
이 그래프를 바탕으로 `행동하는 사회 모델`을 만드는 것이 핵심입니다.

이 흐름을 이해하기 쉽게, 아래처럼 짧은 예시 문서를 가정해보겠습니다.

```text
학생 김민수는 한빛대학교 사회학과에 재학 중이다.
최근 학교의 징계 공지 이후 김민수는 SNS에 공개 비판 글을 올렸다.
이에 대해 한빛대학교는 공식 입장문을 발표했다.
중앙일보는 이 사건을 기사로 보도했고, 일부 동문 단체는 김민수를 지지했다.
```

### 1. 문서가 먼저 그래프로 바뀐다

이 문서를 읽으면 시스템은 먼저 중요한 주체와 관계를 구조화합니다.

예를 들면:

- 주체
  - 김민수
  - 한빛대학교
  - 중앙일보
  - 동문 단체

- 관계
  - 김민수는 한빛대학교 학생이다
  - 김민수는 사건에 대해 글을 올렸다
  - 한빛대학교는 사건에 공식 대응했다
  - 중앙일보는 사건을 보도했다
  - 동문 단체는 김민수를 지지했다

즉, 문서의 서술을 `행위자 + 관계 구조`로 정리한 것이 그래프입니다.

### 2. 그래프의 각 주체가 에이전트가 된다

그 다음 단계에서는 그래프 속 노드들이 시뮬레이션용 에이전트로 바뀝니다.

예를 들면:

- 김민수: 직접 발언하는 당사자
- 한빛대학교: 공식 입장을 내는 기관
- 중앙일보: 이슈를 보도하고 확산시키는 매체
- 동문 단체: 특정 입장을 공개적으로 지지하는 집단

이때 각 에이전트는 단순 이름표가 아니라,  
`어떤 입장인지`, `어떤 식으로 행동할지`, `누구와 가까운지`, `무엇에 반응할지` 같은 정보를 갖게 됩니다.

즉, 그래프의 정적인 노드가 `행동 가능한 디지털 행위자`로 바뀝니다.

### 3. 시뮬레이션 안에서 상호작용이 발생한다

이제 에이전트들이 가상의 소셜 미디어 환경에서 반응하기 시작합니다.

예를 들어 이런 흐름이 생길 수 있습니다.

- 김민수가 추가 비판 글을 올린다
- 한빛대학교가 해명문을 낸다
- 중앙일보가 후속 기사를 낸다
- 동문 단체가 공개 지지 성명을 올린다
- 다른 참여자들이 지지, 반대, 재확산, 무시 같은 반응을 보인다

중요한 점은, 이 단계가 단순 요약이 아니라  
`반응이 또 다른 반응을 낳는 연쇄 과정`을 만들어 본다는 데 있습니다.

즉:

- 학교의 입장문이 논란을 진정시킬 수도 있고
- 오히려 반발을 키울 수도 있고
- 언론 보도가 상황을 장기화시킬 수도 있습니다

### 4. 최종적으로 보고서가 나온다

시뮬레이션이 끝나면 시스템은 어떤 흐름이 만들어졌는지 정리해 보고서를 생성합니다.

예를 들면 보고서에는 이런 식의 설명이 들어갈 수 있습니다.

- 초기에는 학교 비판 여론이 빠르게 확산되었다
- 학교의 첫 공식 대응은 진화 효과가 크지 않았다
- 언론 보도가 사건의 관심도를 유지시켰다
- 동문 단체의 지지가 학생 측 서사를 강화했다
- 추가 대응이 없으면 논란이 장기화될 가능성이 높다

즉, 그래프는 최종 결과물이 아니라  
`예측과 시뮬레이션을 가능하게 하는 기초 구조`입니다.

## 이 부분을 한 줄로 요약하면

문서에서 만든 그래프는 단순 관계도가 아니라,  
이후 에이전트를 만들고 사회적 상호작용을 돌리기 위한 `세계의 뼈대`입니다.

## ontology란 무엇인가

여기서 `ontology`는 철학 용어가 아니라,  
이 프로젝트 안에서는 `이번 문서를 어떤 종류의 주체와 관계로 해석할지 정하는 설계도`라고 보면 됩니다.

쉽게 말하면 ontology는 아래 두 가지를 미리 정합니다.

- 어떤 종류의 엔티티를 볼 것인가
- 어떤 종류의 관계를 볼 것인가

예를 들어 대학 징계 사건 문서라면 ontology는 이런 식으로 잡힐 수 있습니다.

- 엔티티 타입
  - `Student`
  - `Professor`
  - `University`
  - `MediaOutlet`
  - `Person`
  - `Organization`

- 관계 타입
  - `STUDIES_AT`
  - `WORKS_FOR`
  - `REPORTS_ON`
  - `SUPPORTS`
  - `OPPOSES`
  - `RESPONDS_TO`

왜 이게 필요하냐면, ontology 없이 문서를 읽으면 시스템은

- 무엇을 중요한 주체로 볼지
- 어떤 관계만 저장할지
- 어떤 것은 무시할지

기준이 약해집니다.

즉, ontology는 그래프를 만들기 전에 미리 정하는 `분류 기준 + 관계 기준`입니다.

이 프로젝트에서는 LLM이 문서 내용과 사용자의 시뮬레이션 요청을 보고 ontology를 먼저 생성합니다.  
그 다음에야 Zep이 그 기준에 맞춰 실제 노드와 엣지를 채워 넣습니다.

짧게 말하면:

- ontology = 설계도
- graph = 그 설계도로 실제 채워진 관계도

## Zep과 OASIS는 각각 무슨 역할인가

MiroFish는 하나의 거대한 엔진이 아니라, 몇 개의 역할이 분리된 구성입니다.  
그중 가장 중요한 외부 축이 `Zep`과 `OASIS`입니다.

### Zep의 역할

Zep은 이 프로젝트에서 `그래프 메모리/지식 구조 저장소` 역할을 합니다.

쉽게 말하면 Zep은:

- ontology를 받아서
- 문서 chunk들을 읽고
- 노드와 엣지를 만들고
- 그래프를 저장하고
- 나중에 다시 꺼내 읽을 수 있게 해주는 시스템입니다

즉, Zep은 `문서를 구조화된 관계도 형태로 기억하는 계층`입니다.

MiroFish 안에서 Zep은 주로 이런 일에 쓰입니다.

- 그래프 생성
- 노드/엣지 조회
- 특정 엔티티 읽기
- 시뮬레이션 전에 엔티티 목록 추출
- 보고서 생성 시 그래프 기반 검색/조회

### OASIS의 역할

OASIS는 이 프로젝트에서 `에이전트 사회 시뮬레이션 실행기` 역할을 합니다.

쉽게 말하면 OASIS는:

- 그래프에서 뽑아온 주체들을 에이전트로 바꾸고
- Twitter/Reddit 스타일 환경을 구성하고
- 각 에이전트가 어떤 행동을 할지 반복적으로 실행하고
- 라운드별 상호작용을 만들어내는 시스템입니다

즉, OASIS는 `정적인 그래프를 실제로 움직이게 만드는 계층`입니다.

짧게 비교하면:

- Zep = 세계를 저장하는 곳
- OASIS = 그 세계를 움직이는 곳

또는:

- Zep = 관계도/기억
- OASIS = 행동/시뮬레이션

## 프론트엔드와 백엔드에서 어느 파일이 어느 단계를 담당하는가

구조를 가장 단순하게 보면:

- 프론트엔드: 사용자가 단계를 밟는 화면과 API 호출 담당
- 백엔드: 실제 처리 로직 담당

아래처럼 이해하면 전체 코드 구조가 빨리 잡힙니다.

### 1. 앱 시작과 공통 진입점

프론트엔드:

- [frontend/src/main.js](/Users/kwon/gitprojects/MiroFish/frontend/src/main.js)
  Vue 앱 시작점
- [frontend/src/router/index.js](/Users/kwon/gitprojects/MiroFish/frontend/src/router/index.js)
  단계별 화면 라우팅

백엔드:

- [backend/run.py](/Users/kwon/gitprojects/MiroFish/backend/run.py)
  Flask 서버 시작점
- [backend/app/__init__.py](/Users/kwon/gitprojects/MiroFish/backend/app/__init__.py)
  Flask 앱 생성, 블루프린트 등록
- [backend/app/config.py](/Users/kwon/gitprojects/MiroFish/backend/app/config.py)
  `.env` 기반 설정 로딩

### 2. Step 1: 문서 업로드와 ontology 생성

프론트엔드:

- [frontend/src/views/Home.vue](/Users/kwon/gitprojects/MiroFish/frontend/src/views/Home.vue)
  첫 업로드 화면
- [frontend/src/api/graph.js](/Users/kwon/gitprojects/MiroFish/frontend/src/api/graph.js)
  `/api/graph/*` 호출 담당
- [frontend/src/views/MainView.vue](/Users/kwon/gitprojects/MiroFish/frontend/src/views/MainView.vue)
  Step 1과 Step 2를 묶는 메인 작업 화면

백엔드:

- [backend/app/api/graph.py](/Users/kwon/gitprojects/MiroFish/backend/app/api/graph.py)
  업로드, ontology 생성, 그래프 빌드 API
- [backend/app/services/ontology_generator.py](/Users/kwon/gitprojects/MiroFish/backend/app/services/ontology_generator.py)
  문서와 요구사항을 보고 ontology 생성
- [backend/app/utils/file_parser.py](/Users/kwon/gitprojects/MiroFish/backend/app/utils/file_parser.py)
  PDF/TXT/MD 텍스트 추출
- [backend/app/services/text_processor.py](/Users/kwon/gitprojects/MiroFish/backend/app/services/text_processor.py)
  텍스트 전처리와 chunk 분할

### 3. Step 1~2 사이: 그래프 구축

백엔드 핵심:

- [backend/app/services/graph_builder.py](/Users/kwon/gitprojects/MiroFish/backend/app/services/graph_builder.py)
  Zep 그래프 생성, ontology 설정, chunk 업로드, 노드/엣지 조회
- [backend/app/models/project.py](/Users/kwon/gitprojects/MiroFish/backend/app/models/project.py)
  프로젝트 상태, 업로드 파일, 추출 텍스트 저장
- [backend/app/models/task.py](/Users/kwon/gitprojects/MiroFish/backend/app/models/task.py)
  비동기 작업 상태 관리

이 구간이 실제로 `문서 -> 그래프` 변환을 담당합니다.

### 4. Step 2: 시뮬레이션 환경 준비

프론트엔드:

- [frontend/src/views/SimulationView.vue](/Users/kwon/gitprojects/MiroFish/frontend/src/views/SimulationView.vue)
  환경 준비 화면
- [frontend/src/api/simulation.js](/Users/kwon/gitprojects/MiroFish/frontend/src/api/simulation.js)
  `/api/simulation/*` 호출 담당

백엔드:

- [backend/app/api/simulation.py](/Users/kwon/gitprojects/MiroFish/backend/app/api/simulation.py)
  엔티티 조회, 시뮬레이션 생성/준비/실행 API
- [backend/app/services/zep_entity_reader.py](/Users/kwon/gitprojects/MiroFish/backend/app/services/zep_entity_reader.py)
  Zep 그래프에서 실제 엔티티 읽기
- [backend/app/services/oasis_profile_generator.py](/Users/kwon/gitprojects/MiroFish/backend/app/services/oasis_profile_generator.py)
  엔티티를 OASIS용 Agent Profile로 변환
- [backend/app/services/simulation_config_generator.py](/Users/kwon/gitprojects/MiroFish/backend/app/services/simulation_config_generator.py)
  라운드 수, 시간 설정, 에이전트 활동성 등 시뮬레이션 파라미터 생성
- [backend/app/services/simulation_manager.py](/Users/kwon/gitprojects/MiroFish/backend/app/services/simulation_manager.py)
  준비 단계 전체 orchestration

이 구간은 `그래프 -> 시뮬레이션 가능한 에이전트 사회`를 만드는 단계입니다.

### 5. Step 3: 시뮬레이션 실행

프론트엔드:

- [frontend/src/views/SimulationRunView.vue](/Users/kwon/gitprojects/MiroFish/frontend/src/views/SimulationRunView.vue)
  실행 상태, 진행 상황, 로그 표시

백엔드:

- [backend/app/services/simulation_runner.py](/Users/kwon/gitprojects/MiroFish/backend/app/services/simulation_runner.py)
  OASIS 시뮬레이션 실제 실행, 상태 추적, 최근 액션 수집
- [backend/scripts/run_parallel_simulation.py](/Users/kwon/gitprojects/MiroFish/backend/scripts/run_parallel_simulation.py)
  병렬 시뮬레이션 스크립트
- [backend/scripts/run_twitter_simulation.py](/Users/kwon/gitprojects/MiroFish/backend/scripts/run_twitter_simulation.py)
  Twitter 스타일 시뮬레이션
- [backend/scripts/run_reddit_simulation.py](/Users/kwon/gitprojects/MiroFish/backend/scripts/run_reddit_simulation.py)
  Reddit 스타일 시뮬레이션

이 구간이 실제로 에이전트들을 움직이는 부분입니다.

### 6. Step 4: 보고서 생성

프론트엔드:

- [frontend/src/views/ReportView.vue](/Users/kwon/gitprojects/MiroFish/frontend/src/views/ReportView.vue)
  보고서 생성/열람 화면
- [frontend/src/api/report.js](/Users/kwon/gitprojects/MiroFish/frontend/src/api/report.js)
  `/api/report/*` 호출 담당

백엔드:

- [backend/app/api/report.py](/Users/kwon/gitprojects/MiroFish/backend/app/api/report.py)
  보고서 생성, 상태 조회, 대화 API
- [backend/app/services/report_agent.py](/Users/kwon/gitprojects/MiroFish/backend/app/services/report_agent.py)
  Report Agent의 기획, 툴 호출, 섹션별 보고서 생성
- [backend/app/services/zep_tools.py](/Users/kwon/gitprojects/MiroFish/backend/app/services/zep_tools.py)
  Report Agent가 그래프를 탐색할 때 쓰는 도구 계층

이 구간은 `시뮬레이션 로그 -> 분석 보고서`로 바꾸는 단계입니다.

### 7. Step 5: 심화 상호작용

프론트엔드:

- [frontend/src/views/InteractionView.vue](/Users/kwon/gitprojects/MiroFish/frontend/src/views/InteractionView.vue)
  보고서 이후 대화 화면

백엔드:

- [backend/app/api/report.py](/Users/kwon/gitprojects/MiroFish/backend/app/api/report.py)
  Report Agent와의 채팅
- [backend/app/api/simulation.py](/Users/kwon/gitprojects/MiroFish/backend/app/api/simulation.py)
  시뮬레이션 내 Agent 인터뷰 관련 API

이 구간에서는 사용자가 결과를 더 캐묻고, 특정 에이전트와 직접 상호작용할 수 있습니다.

## 구조를 가장 짧게 요약하면

이 코드베이스는 아래처럼 나눠서 보면 됩니다.

- ontology: 문서를 어떤 종류의 주체/관계로 읽을지 정하는 설계도
- Zep: 그 설계도에 따라 그래프를 저장하고 조회하는 계층
- OASIS: 그래프를 바탕으로 에이전트를 움직이는 시뮬레이션 계층
- frontend: 이 전체 과정을 5단계 UI로 보여주는 계층
- backend: 실제 추출, 변환, 실행, 보고서 생성을 담당하는 계층

## 이 시스템은 1회성인가, 저장했다가 다시 쓸 수 있는가

완전히 1회성인 구조는 아닙니다.  
이 코드베이스는 `프로젝트`, `그래프`, `시뮬레이션 상태`, `보고서`를 어느 정도 저장해 두고 다시 불러올 수 있게 만들어져 있습니다.

다만, 무엇이 저장되고 무엇이 일시적인지는 구분해서 보는 것이 좋습니다.

### 저장되는 것

#### 1. 프로젝트 정보

사용자가 문서를 업로드하면 프로젝트가 생성되고, 관련 정보가 파일로 저장됩니다.

예를 들면:

- 프로젝트 ID
- 업로드한 파일 목록
- 추출된 텍스트
- ontology
- graph_id

즉, 한 번 문서를 올려 프로젝트를 만들면,  
나중에 다시 들어와도 그 프로젝트의 기본 정보는 남아 있습니다.

#### 2. 그래프

그래프는 Zep에 생성되고 `graph_id`로 관리됩니다.

즉:

- 문서에서 만든 관계도는 Zep에 저장되고
- 프로젝트 쪽에는 그 그래프를 가리키는 `graph_id`가 남습니다

그래서 나중에 같은 프로젝트를 다시 열면,  
이미 만든 그래프를 다시 조회해서 보여줄 수 있습니다.

#### 3. 시뮬레이션 상태와 결과

시뮬레이션도 완전히 날아가는 구조는 아닙니다.

코드상으로는 시뮬레이션별 디렉터리에 상태 파일이 저장됩니다.

예를 들면:

- `state.json`
- `run_state.json`
- 시뮬레이션 중 생성된 각종 데이터 파일

즉, 어떤 시뮬레이션이 생성되었는지, 어떤 설정으로 준비되었는지,  
어느 정도 결과가 나왔는지는 다시 확인할 수 있습니다.

#### 4. 보고서

보고서도 저장됩니다.

보고서는 보통 `reports/{report_id}` 형태의 폴더에 저장되고,  
그 안에 보고서 본문과 로그가 함께 남습니다.

즉:

- 한 번 생성한 보고서를 다시 열람할 수 있고
- 같은 simulation에 대해 기존 보고서를 재사용하는 흐름도 있습니다

### 일시적이거나 약한 부분

#### 1. 실시간 진행 상태

그래프 생성 중 퍼센트, 보고서 생성 중 현재 단계 같은 `실시간 task 진행 상태`는 비교적 일시적입니다.

이 부분은 메모리 기반 관리가 포함되어 있어서:

- 서버가 살아 있는 동안에는 잘 보이지만
- 서버가 재시작되면 진행 중 task 정보는 자연스럽게 끊길 수 있습니다

즉, `완료된 결과`는 남더라도 `진행 중이던 퍼센트 표시`는 영구 보존되는 구조가 아닙니다.

#### 2. 실행 중 프로세스 자체

시뮬레이션이 한창 돌아가는 중에 서버가 내려가거나 프로세스가 끊기면,  
일반적인 의미의 강력한 `resume from checkpoint` 구조라고 보기는 어렵습니다.

상태 파일은 남아도, 정확히 그 시점부터 자연스럽게 이어 실행되는 보장은 약합니다.

즉:

- 결과 저장은 어느 정도 됨
- 실행 중 프로세스 복원은 강하지 않음

### 실제 사용 감각으로 보면

실제 사용자는 보통 이렇게 이해하면 됩니다.

1. 문서를 올려 프로젝트를 만든다
2. 그래프를 만든다
3. 시뮬레이션을 준비하고 실행한다
4. 보고서를 생성한다
5. 나중에 다시 들어와서 프로젝트/그래프/보고서를 다시 볼 수 있다

즉, `업로드하고 끝나는 완전 1회성 툴`은 아닙니다.  
오히려 `프로젝트 단위로 저장되는 작업형 시스템`에 더 가깝습니다.

다만, `장시간 실행 중 작업을 언제든 정확히 이어받는 워크플로 엔진` 수준은 아니라고 보는 편이 맞습니다.

## 한 줄 요약

MiroFish는 완전 1회성은 아니고,  
프로젝트/그래프/시뮬레이션 결과/보고서를 저장했다가 다시 조회할 수 있습니다.  
다만 진행 중 작업과 실행 중 프로세스의 완전한 재개까지 강하게 보장하는 구조는 아닙니다.
