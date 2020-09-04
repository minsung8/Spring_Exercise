# Spring_Exercise

Spring Framework
- 엔터프라이즈 어플리케이션을 구축할 수 있는 가벼운 솔루션
- 원하는 부분만 사용할 수 있도록 모듈화
- IoC 컨테이너
- 선언적으로 트랜잭션 관리 가능
- 완전한 기능을 갖춘 MVC Framework 제공
- AOP 지원
- 도메인 논리코드와 쉽게 분리가능한 구조

AOP와 Instrumentation
- Spring-AOP : AOP 얼라이언스와 호환하는 방법으로 AOP 지원
- Spring-aspect : Aspectj와의 통합 제공
- Spring-instrument : Instrumentation을 지원하는 클래스와 특정 WAS에서 사용하는 클래스로 더 구현체를 제공

Messaging
- Spring-message : 메시지 기반 어플리케이션을 작성할 수 있는 Message, MessageChannel, MessageHandler 등을 제공

Data Access / Integration 
- 데이터 엑세스/통합 계층은 JDBC, ORM, OXM, JMS 및 트랜잭션 모듈로 구성
- spring-jdbc : 자바 JDBC프로그래밍을 쉽게 할 수 있도록 기능을 제공
- spring-tx : 선언적 트랜잭션 관리를 할 수 있는 기능을 제공
- spring-orm : JPA, JDO및 Hibernate를 포함한 ORM API를 위한 통합 레이어를 제공
- spring-oxm : JAXB, Castor, XMLBeans, JiBX 및 XStream과 같은 Object/XML 맵핑을 지원
- spring-jms : 메시지 생성(producing) 및 사용(consuming)을 위한 기능을 제공, Spring Framework 4.1부터 spring-messaging모듈과의 통합을 제공

Web
- 웹 계층은 spring-web, spring-webmvc, spring-websocket, spring-webmvc-portlet 모듈로 구성
- spring-web : 멀티 파트 파일 업로드, 서블릿 리스너 등 웹 지향 통합 기능을 제공한다. HTTP클라이언트와 Spring의 원격 지원을 위한 웹 관련 부분을 제공
- spring-webmvc : Web-Servlet 모듈이라고도 불리며, Spring MVC 및 REST 웹 서비스 구현을 포함
- spring-websocket : 웹 소켓을 지원
- spring-webmvc-portlet : 포틀릿 환경에서 사용할 MVC 구현을 제공

ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ

컨테이너 (Container)
- 컨테이너는 인스턴스의 생명주기 관리 및 추가적인 기능 제공

IoC(Inversion of Control)
- 컨테이너가 코드 대신 오브젝트의 제어권을 가지고 있는 것을 의미

DI (Dependency Injection)
- 클래스 사이의 의존관계를 bean 설정정보를 바탕으로 컨테이너가 자동으로 연결해주는 것을 의미 

Spring 에서 제공하는 IoC/DI 컨테이너 
- BeanFactory : Ioc/DI에 대한 기본 기능을 가지고 있음
- ApplicationContext : BeanFactory의 모든 기능을 포함하며 BeanFactory보다 추천됨. 트랜잭션처리, AOP등에 대한 처리 및 BeanPostProcessor, BeanFactoryPostProcessor등을 자동으로 등록하고, 국제화 처리, 어플리케이션 이벤트 등을 처리할 수 있음

Bean class
- 일반적으로 java class를 의미
- 3가지 특징 
  1. 기본생성자를 가진다
  2. 필드는 private 선언
  3. getter, setter 메서드를 가진다 => Property

Java Config을 이용한 설정을 위한 어노테이션
  @Configuration => 스프링 설정 클래스를 선언하는 어노테이션
  @Bean => bean을 정의하는 어노테이션
  @ComponentScan => @Controller, @Service, @Repository, @Component 어노테이션이 붙은 클래스를 찾아 컨테이너에 등록
  @Component => 컴포넌트 스캔의 대상이 되는 애노테이션 중 하나로써 주로 유틸, 기타 지원 클래스에 붙이는 어노테이션
  @Autowired => 주입 대상이되는 bean을 컨테이너에 찾아 주입하는 어노테이션
  
  ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ

테스팅 (Testing)
- 응용프로그램 또는 시스템의 동작과 성능, 안정성 등이 요구하는 수준을 만족하는지 확인하기 위해 결함을 발견하는 과정 
- 정적 테스트 => 프로그램을 개발하기 전에 요구사항등을 리뷰하는 것
- 동적 테스트 => 프로그램 개발 이후 실제 실행하면서 테스트하는 것
  
소프트웨어에서 테스트가 필요한 이유
  1) 금전적인 손실
  2) 시간 낭비
  3) 비즈니스의 이미지 손상
  4) 부상이나 사망
  등의 문제를 최소화하기 위해 필요


테스트 역할

  1) 테스팅을 통해 릴리즈 전에 발견되지 않은 결함들이 수정된다면, 
  운영 환경 내에서 발생하는 리스크(risk)를 줄이는데 기여할 수 있으며 
  소프트웨어 품질에 도움을 줍니다.

  2) 테스팅은 개발 초기의 요구사항 분석 단계부터 리뷰 및 인스펙션을 통해 정적으로 이뤄질 수 있으며
  각각의 개발 단계에 대응하는 테스트 레벨(test level)에 따른 테스팅이 이뤄집니다.

  3) 기존에 운영되는 소프트웨어 시스템이 유지 보수 활동으로 변경 및 단종되거나 
  환경이 변하는 경우, 변경된 소프트웨어에 대한 테스팅과 
  변경된 환경에서의 운영 테스팅이 요구됩니다.

  4) 소프트웨어 테스팅은 계약상(법적) 요구조건들, 또는 산업에 특화된 표준들을 만족시키기 위해서 필요합니다.


테스팅의 원리

  원리 1 – 테스팅은 결함이 존재함을 밝히는 활동이다.
  테스팅은 결함이 존재함을 드러내지만, 결함이 없다는 것을 증명할 수 없습니다. 
  즉, 프로그램이 완벽하다고 증명할 수 없습니다. 
  이는 테스트 한 부분까지만 잘 동작한다고 말할 수 있고 테스트를 하지 않은 부분은
  결함 있는지 또는 없는지에 대해서 예측할 수 없다는 의미입니다.

  원리 2 – 완벽한 테스팅(Exhaustive testing)은 불가능하다.
  모든 가능성(입력과 사전 조건의 모든 조합)을 테스팅하는 것은 지극히 간단한 소프트웨어를 제외하고 가능하지 않습니다.
  보통 다음과 같은 이유 때문입니다.

    - 한 프로그램 내의 내부 조건이 무수히 많음. (무한 경로)
    - 입력이 가질 수 있는 모든 값의 조건이 무수히 많음 (무한 입력 값)
    - GUI 이벤트 발생 순서에 대한 조합도 무수히 많음 (무한 타이밍)

  완벽한 테스팅 대신, 리스크 분석과 결정된 우선순위에 따라 테스팅 활동 노력을 집중시켜야 합니다. (Risk-based testing) 
  완벽한 테스팅은 우주항공, 의료 등 안전이 최우선(Safety critical)인 소프트웨어를 개발할 때 고려할 수 있으나
  실제로 완벽한 것은 아니고 강력한 테스팅으로 볼 수 있습니다.

  원리 3 – 테스팅을 개발 초기에 시작한다.
  테스팅 활동은 소프트웨어나 시스템 개발 수명주기에서 가능한 초기에 시작되어야 하며, 
  설정한 테스팅 목표에 집중해야 합니다. 
  개발 초기에 테스팅을 시작한다는 것의 의미는 개발의 시작과 동시에 테스트를 계획하고
  전략적으로 접근하는 것을 고려하는 것은 물론, 요구사항 분석서와 설계서 등의 개발 중간 산출물을 분석하여
  테스트하는 것을 의미합니다.


  
  
  

  












