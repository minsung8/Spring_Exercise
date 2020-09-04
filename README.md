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
  
  

  












