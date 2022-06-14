# 소프트웨어 공학 기말 정리
---------------------------------
## 상위 설계, 하위 설계
- 상위 설계 - 아키텍쳐 설계, 데이터 설계, 인터페이스 정의, 사용자 인터페이스 설계   
- 하위 설계 - 모듈 설계, 자료구조 설계, 알고리즘 설계   
---------------------------------
### 상위 설계
- 아키텍쳐 설계 : 시스템의 전체적인 구조   
- 데이터 설계 : 시스템에 필요한 정보를 자료구조와 데이터베이스 설계에 반영   
- 시스템 분할 : 전체 시스템을 여러 개의 서브 시스템으로 나눈다.   
- 인터페이스 정의 : 시스템의 구조와 서브 시스템들 사이의 인터페이스가 명확히 정의   
- UI 설계 : 사용자가 익숙하고 편리하게 사용할 수 있도록 사용자 인터페이스 정의   
---------------------------------
### 하위 설계
- 각 모듈의 실제적인 내부를 알고리즘 형태로 표현   
- 각 인터페이스에 대한 설명, 자료구조, 변수 등에 대한 상세한 정보를 작성   

---------------------------------
## 분할과 정복
- 큰 문제를 소 단위로 나누고 소 단위의 작업을 하나씩 처리하여 전체 일을 끝내는 방법
### 분할 형태
- 분산 시스템은 클라이언트와 서버로 분할   
- 시스템은 여러 서브 시스템으로 분할   
- 서브 시스템은 하나 이상의 패키지로 분할   
- 패키지는 여러 클래스로 분할   
- 클래스는 여러 메소드로 분할   
---------------------------------
## 추상화
- 현재의 관심사에 초점을 맞추기 위해, 특정한 목적과 관련된 필수 정보만 추출하여 강조하고 관련이 없는 세부 사항을 생략함으로써 본질적인 문제에 집중할 수 있도록 하는 작업   
- 객체 지향 설계에서의 추상화란 객체둘의 공통점을 뽑아 클래스라는 이름을 붙여놓은 것
### 추상화의 종류
- 1. 과정 추상화   
> - Class의 특징 : 사용자에게 클래스가 제공할 수 있는 사용법만 알려주고, 불필요한 데이터와 연산을 감춤   
- 2. 데이터 추상화   
- 3. 제어 추상화   
---------------------------------
## 단계적 분해
- 하향식 설계에서 사용한다.   
- 기능을 점점 작은 단위로 나누어 점차적으로 구체화 하는 방법이다.   

---------------------------------
## 모듈화
### 모듈
- 규모가 큰 것을 여러개로 나눈 조각   
- 소프트웨어 구조를 이루는 기본적인 단위   
- 하나 또는 몇 개의 논리적인 기능을 수행하기 위한 명령어들의 집합   
### 모듈의 특징
- 다른 것들과 구별될 수 있는 *독립적인* 기능을 갖는 단위   
- 유일한 이름을 가져야한다.   
- 독립적으로 컴파일이 가능하다.   
- 모듈에서 또 다른 모듈을 호출할 수 있다.   
- 다른 프로그램에서도 모듈을 호출할 수 있다.   
### 모듈 vs 컴포넌트
- 모듈이란 비슷하거나 연관성 있는 것들로 이루어진 메소드나 클래스의 집합   
- 컴포넌트란 기능의 최소 단위이다. 소프트웨어를 재사용하기 위한 일종의 개발 방법이다.
#### 모듈과 컴포넌트의 차이점
>- 모듈은 구조의 최소 단위, 정적인 구조를 가짐   
>- 컴포넌트는 런타임에 독립적으로 배포되고 실행되는 단위. 즉, 실행중인 소프트웨어의 활동단위, 동적인 구조를 가짐   
---------------------------------
## 이해 관계자별 품질 속성
### 발주자 관점   
- 제품 가 (또는 개발비)이 중요, 응찰 시 가장 적게 써낸 업체 선정 확률이 높음   
### 사용자 관점
- 완벽한 기능뿐만 아니라 사용하기 쉽고 빨리 이해할 수 있는 아키텍처의 속성을 요구   
### 개발자 관점
- 플랫폼이 달라져도 새로운 플랫폼에 쉽게 적용할 수 있는 아키텍처의 속성에 관심   
- 변경 요청 시 쉽게 변경할 수 있는 설계

---------------------------------
## 아키텍쳐 4+1 관점
- 논리적관점, 구현관점, 프로세스 관점, 배치관점 + 유스케이스 관점이 있다.   
   
### 유즈케이스 관점 (usecase view)
- 사용자 기능   
- 시스템이 사용자에게 제공하는 기능에 관심   
- 다른 네 가지 관점에 사용되는 다이어그램의 근간   
>- 정적표현 : 유스케이스 다이어그램   
>- 동적표현 상태 다이어그램, 순차 다이어그램, 통신 다이어그램, 활동 다이어그램   
   
### 논리적 관점 (logical view)
- 분석가/설계자 : 클래스나 컴포넌트의 종류와 관계   
- 클래스나 컴포넌트의 종류와 이들의 관계에 초점   
>- 정적표현 : 클래스 다이어그램, 객체 다이어그램   
>- 동적표현 : 상태 다이어그램, 순차 다이어그램, 통신 다이어그램, 활동 다이어그램   
   
### 구현 관점 (implementation view)
- 프로그래머 : 서브 시스템의 모듈 구조와 관계   
- 소프트웨어 서브시스템의 모듈이 어떻게 구조화 되어있는가에 관심   
>- 정적표현 : 컴포넌트 다이어그램   
>- 동적표현 : 상태 다이어그램, 순차 다이어그램, 통신 다이어그램, 활동 다이어그램   
   
### 프로세스 관점 (process view)
- 시스템 통합자 : 시스템의 성능, 확장성, 효율   
- 실제 구동 환경을 살펴봄으로써 논리적 관점과 같이 시스템 내부의 구조에 초점   
- 시스템의 동시성과 동기화에 관심   
   
### 배치 관점 (deployment view)
- 시스템 엔지니어 : 시스템의 구성   
- 시스템을 구성하는 처리 장치 간의 물리적인 배치에 초점   
- 서브 시스템들이 물리적인 환경에서 어떻게 연관되어 실행되는지를 나타냄   
- 시스템의 분산 구조와 실행할 때 컴포넌트들의 배치 상태를 나타냄   
>- 정적표현 : 배치 다이어그램   
>- 동적표현 : 상태 다이어그램, 순차 다이어그램, 통신 다이어그램, 활동 다이어그램   
---------------------------------
## 아키텍쳐 모델
- 아키텍처 모델은 크게 두 분류이다. 기능의 분할과 배치, 제어 관계   
>- 기능의 분할과 배치 : 데이터 중심형 모델, 클라이언트-서버 모델, 계층모델, MVC모델   
>- 제어 관계 : 데이터 흐름 모델   

### 데이터 중심 모델 (repository model)
- 특징 : 주요 데이터가 repository에서 중앙 관리   
- 구성 : repository와 여기에 접근하는 서브 시스템   
- 장점   
>- 데이터가 한군데 모여 있기 때문에 데이터를 모순되지 않고 일관성 있게 관리 가능   
>- 새로운 서브 시스템의 추가 용이   
- 단점   
>- repository의 병목 현상 발생 가능   
>- 서브 시스템과 repository 사이의 강한 결합(repository 변경 시 서브 시스템에 영향을 줌)   

### 클라이언트-서버 모델 (client-server model)
- 네트워크를 이용한 분산 시스템 형태   
- 데이터와 처리 기능을 클라이언트와 서버에 분할하여 사용   
- 분산 아키텍쳐에 유용   
>- 서버 : 클라이언트(서브시스템)에 서비스 제공   
>- 클라이언트 : 서버가 제공하는 서비스를 요청(호출)하는 서브 시스템   

### 계층 모델 (layering model)
- 기능을 몇 개의 계층으로 나누어 배치   
- 구성 : 하위 계층은 서버, 상위 계층은 클라이언트 역할   
- 장점   
>- 구조가 간단하고, 판독이 용이하다.   
>- 구현, 수정, 검색이 용이하다.   
>- 망 데이터 모델이나 관계 데이터 모델도 실제로 구현할 때는 계층적인 기억 구조를 이용   
- 단점   
>- 데이터 상호간의 유연성이 부족하다.   
>- 검색 경로가 한정되어 있다.   
>- 삽입과 삭제 연산이 매우 복잡하다   
>- 다 대 다 관계를 처리하기 어렵다.   

### MVC 모델 (model-view-controller model)
- 중앙 데이터 구조   
- 같은 모델의 서브 시스템에 대하여 여러 뷰 서브 시스템을 필요로 하는 시스템에 적합   
- 세 개의 서브시스템으로 분리하는 이유 : 변경에 대한 영향을 덜 미치도록 하기 위해 -> 즉 UI부분이 자주 변경 되더라도 모델 서브 시스템에는 영향을 주지 않기 위해    

#### Model 서브 시스템
- 뷰/제어 서브시스템과 독립되어 모든 데이터 상태와 로직을 처리   
- 특정 입, 출력 방식에 영향을 받지 않고, 무언가의 호출에 응답만 함.   

#### View 서브 시스템
- 사용자와 직접 대화가 이루어지는 부분으로 데이터 처리를 사용자에게 보여주는 역할   

#### Controller 서브 시스템
- 뷰를 통한 사용자의 요청을 적정한 모델 쪽으로 넘겨주고, 모델로부터 받은 응답을 다시 뷰를 통해 사용자에게 돌려주는 역할   

- 장점   
>- 관심의 분리   
>- 데이터를 화면에 표현하는 디자인(뷰)과 로직(모델)을 분리함으로써 느슨한 결합 가능   
>- 구조 변경 요청 시 수정이 용이   
- 단점   
>- 기본 기능 설계로 인한 클래스 수의 증가로 복잡도 증가   
>- 속도가 중요한 프로젝트에 부적합   

### 데이터 흐름 모델
- Pipe and filter 구조   
>- Filter : data stream을 한 개 이상 입력 받아 처리(변환)한 후 data stream 하나를 출력   
>- pipe : filter를 거쳐 생성된 data stream 하나를 다른 filter의 입력에 연결   

---------------------------------
## 디자인 패턴
- 자주 사용하는 설계 형태를 정형화해서 이를 유형별로 설계 템플릿을 만들어둔 것    
- 많은 개발자들이 경험상 체득한 설계 지식을 검증하고 이를 추상화하여 일반화한 템플릿   

### 장점
- 개발자(설계자)간의 원활한 의사소통    
- 소프트웨어 구조 파악 용이   
- 재사용을 통한 개발 시간 단축   
- 설계 변경 요청에 대한 유연한 대처   

### 단점
- 객체지향 설계/구현 위주   
- 초기 투자 비용 부담   

### 생성 패턴
#### 기능
- 객체를 생성하는 것과 관련된 패턴으로 객체의 생성과 변경이 전체 시스템에 미치는 영향을 최소화하도록 만들어주어 유연성을 높일 수 있고 코드를 유지하기가 쉬운 편이다. 객체의 생성과 참조 과정을 추상화함으로써 시스템을 개발할 때 부담을 덜어준다.   
#### 종류
- factory method 패턴   
>- 상위 클래스에서 객체를 생성하는 인터페이스를 정의하고, 하위 클래스에서 인스턴스를 생성하도록 하는 방식   
>- 객체를 생성하는 시점은 알지만 어떤 객체를 생성해야 할지 알 수 없을 때, 객체 생성을 하위 클래스에 위임하여 해결   
   
- singleton 패턴   
>- 특정 클래스의 객체가 오직 한 개만 존재하도록 보장, 즉 클래스의 객체를 하나로 제한   
>- 동일한 자원이나 데이터를 처리하는 객체가 불필요하게 여러 개 만들어질 필요가 없는 경우에 주로 사용   
   
- prototype 패턴   
>- new Object() 보다 clone()을 이용해 기존의 것을 복사하여 일부만 바꿔 인스턴스 생성   
>- 일반적인 prototype(원형)을 만들어놓고, 그것을 복사한 후 필요한 부분만 수정하여 사용   
>- 인스턴스를 복제하여 사용하는 구조   
>- 생성할 객체의 원형을 제공하는 프로토타입 인스턴스로부터 생성할 객체들의 타입 결정   
>- 객체를 생성할 때 갖추어야할 기본 형태가 있을 때 사용   
   
- builder 패턴   
>- 복잡한 인스턴스를 조립하여 만드는 구조   
>- 복합 객체를 생성할 때 객체를 생성하는 방법(과정)과 객체를 구현(표현)하는 방법을 분리   
>- 동일한 생성 절차에서 서로 다른 표현 결과를 만들 수 있다.   
   
- abstract factory 패턴   
>- 구체적인 구현은 concreateProduct 클래스에서 이루어짐   
>- 사용자에게 API를 제공하고, 인터페이스만 사용해서 부품을 조립하여 만든다. 즉 추상적인 부품을 조합해서 추상적인 제품을 만든다.   


### 구조 패턴
#### 기능
- 프로그램 내의 자료구조나 인터페이스 구조를 설계하는 데 많이 활용할 수 있는 패턴이다. 클래스나 객체들의 구성(합성)을 통해서 더 큰 구조로 만들 수 있게 해준다. 규모가 큰 시스템은 많은 클래스로 구성되어 복잡한 구조를 갖는다. 이렇게 구조가 복잡하면 수정이 쉽지 않다. 또 수정으로 인한 오류도 많이 발생할 수 있다. 이렇게 복잡한 형태의 구조를 갖는 시스템을 개발하기 쉽게 만들어주는 패턴이 바로 구조 패턴이다. 따라서 구조 패턴을 이용하면 새로운 기능을 가진 복합 객체를 효과적으로 작성할 수 있다.   
#### 종류
- adapter
>- 기존 클래스를 재사용할 수 있도록 중간에서 맞춰주는 역할   
>- 호환성이 없는 기존 클래스의 인터페이스를 변환해 재사용할 수 있도록 해준다.   

   
- composite   
>- 사용자가 단일 객체와 복합 객체 모두 동일하게 다루도록 한 것   
>- 재귀적 구조 : 디렉토리 안에 파일 또는 다른 디렉토리(서브 디렉토리)가 존재할 수 있는 것   
>- 그릇(디렉토리)과 내용물(파일)을 동일시해서 재귀적인 구조를 만들기 위한 설계 패턴   
   
- bridge   
- facade   
- flywieght   
- proxy   

### 행위 패턴
#### 기능
- 반복적으로 사용되는 객체들의 상호작용을 패턴화한 것으로, 클래스나 객체들이 상호작용하는 방법과 책임을 분산하는 방법을 정의한다. 객체의 기능은 변하지 않지만 일을 처리하는 방법이 달라질 때가 있다. 응용 분야에 따라 행위가 다른 객체로 옮겨 가거나 알고리즘이 대체되는 경우이다. 그런 경우 대부분 상속 개념을 이용해 사용할 수 있다. 행위 패턴은 여러 가지 행위 관련 패턴을 사용하여 독립적으로 일을 처리하고자 할 때 사용한다. 즉 행위 패턴은 메세지 교한과 관련된 것으로, 객체들 간의 행위나 알고리즘 등과 관련된 패턴을 말한다.   
#### 종류
- template method   
- interpreter   
- iterator   
- observer   
- strategy   
- visitor   
- chain of responsibility   
- command   
- mediator   
- state   
- memento   