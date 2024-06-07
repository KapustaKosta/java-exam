- [1. Многопоточность](#1-%D0%9C%D0%BD%D0%BE%D0%B3%D0%BE%D0%BF%D0%BE%D1%82%D0%BE%D1%87%D0%BD%D0%BE%D1%81%D1%82%D1%8C)
		- [1. Создание потоков: использование `Thread` и `Runnable`](#1-%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%B2-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-thread-%D0%B8-runnable)
		- [2. Расширенные возможности потоков: использование `Callable` и `Future`](#2-%D0%A0%D0%B0%D1%81%D1%88%D0%B8%D1%80%D0%B5%D0%BD%D0%BD%D1%8B%D0%B5-%D0%B2%D0%BE%D0%B7%D0%BC%D0%BE%D0%B6%D0%BD%D0%BE%D1%81%D1%82%D0%B8-%D0%BF%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%B2-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-callable-%D0%B8-future)
		- [3. Синхронизация: ключевое слово `synchronized`, проблемы гонки и deadlock](#3-%D0%A1%D0%B8%D0%BD%D1%85%D1%80%D0%BE%D0%BD%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F-%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%B2%D0%BE%D0%B5-%D1%81%D0%BB%D0%BE%D0%B2%D0%BE-synchronized-%D0%BF%D1%80%D0%BE%D0%B1%D0%BB%D0%B5%D0%BC%D1%8B-%D0%B3%D0%BE%D0%BD%D0%BA%D0%B8-%D0%B8-deadlock)
		- [4. Locks: использование `Lock`, `ReentrantLock`](#4-locks-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-lock-reentrantlock)
		- [5. Высокоуровневые конструкции: `ExecutorService`](#5-%D0%92%D1%8B%D1%81%D0%BE%D0%BA%D0%BE%D1%83%D1%80%D0%BE%D0%B2%D0%BD%D0%B5%D0%B2%D1%8B%D0%B5-%D0%BA%D0%BE%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%86%D0%B8%D0%B8-executorservice)
		- [6. Конкурентные коллекции: `ConcurrentHashMap`, `CopyOnWriteArrayList`](#6-%D0%9A%D0%BE%D0%BD%D0%BA%D1%83%D1%80%D0%B5%D0%BD%D1%82%D0%BD%D1%8B%D0%B5-%D0%BA%D0%BE%D0%BB%D0%BB%D0%B5%D0%BA%D1%86%D0%B8%D0%B8-concurrenthashmap-copyonwritearraylist)
- [2. Системы сборки](#2-%D0%A1%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B-%D1%81%D0%B1%D0%BE%D1%80%D0%BA%D0%B8)
		- [1. Maven: конфигурация проекта в `pom.xml`, жизненный цикл сборки](#1-maven-%D0%BA%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D1%83%D1%80%D0%B0%D1%86%D0%B8%D1%8F-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0-%D0%B2-pomxml-%D0%B6%D0%B8%D0%B7%D0%BD%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9-%D1%86%D0%B8%D0%BA%D0%BB-%D1%81%D0%B1%D0%BE%D1%80%D0%BA%D0%B8)
		- [2. Зависимости в Maven: управление иерархией зависимостей, репозитории](#2-%D0%97%D0%B0%D0%B2%D0%B8%D1%81%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B8-%D0%B2-maven-%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B8%D0%B5%D1%80%D0%B0%D1%80%D1%85%D0%B8%D0%B5%D0%B9-%D0%B7%D0%B0%D0%B2%D0%B8%D1%81%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B5%D0%B9-%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B8)
		- [3. Gradle: написание `build.gradle` скриптов](#3-gradle-%D0%BD%D0%B0%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-buildgradle-%D1%81%D0%BA%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%B2)
		- [4. Задачи в Gradle: создание и запуск пользовательских задач](#4-%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B8-%D0%B2-gradle-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B8-%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA-%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D1%81%D0%BA%D0%B8%D1%85-%D0%B7%D0%B0%D0%B4%D0%B0%D1%87)
		- [5. Плагины: использование и конфигурация плагинов в Maven и Gradle](#5-%D0%9F%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D1%8B-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B8-%D0%BA%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D1%83%D1%80%D0%B0%D1%86%D0%B8%D1%8F-%D0%BF%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D0%BE%D0%B2-%D0%B2-maven-%D0%B8-gradle)
- [3. IoC и DI (Inversion of Control и Dependency Injection)](#3-ioc-%D0%B8-di-inversion-of-control-%D0%B8-dependency-injection)
		- [1. Основы IoC: принципы инверсии управления](#1-%D0%9E%D1%81%D0%BD%D0%BE%D0%B2%D1%8B-ioc-%D0%BF%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF%D1%8B-%D0%B8%D0%BD%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D0%B8-%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F)
		- [2. Типы DI: конструкторная, сеттерная, интерфейсная инъекции](#2-%D0%A2%D0%B8%D0%BF%D1%8B-di-%D0%BA%D0%BE%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F-%D1%81%D0%B5%D1%82%D1%82%D0%B5%D1%80%D0%BD%D0%B0%D1%8F-%D0%B8%D0%BD%D1%82%D0%B5%D1%80%D1%84%D0%B5%D0%B9%D1%81%D0%BD%D0%B0%D1%8F-%D0%B8%D0%BD%D1%8A%D0%B5%D0%BA%D1%86%D0%B8%D0%B8)
		- [3. Spring IoC контейнер: использование аннотаций `@Component`, `@Autowired`](#3-spring-ioc-%D0%BA%D0%BE%D0%BD%D1%82%D0%B5%D0%B9%D0%BD%D0%B5%D1%80-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B0%D0%BD%D0%BD%D0%BE%D1%82%D0%B0%D1%86%D0%B8%D0%B9-component-autowired)
		- [4. Singleton и Prototype: scoping биннов в Spring](#4-singleton-%D0%B8-prototype-scoping-%D0%B1%D0%B8%D0%BD%D0%BD%D0%BE%D0%B2-%D0%B2-spring)
		- [5. Конфигурации: способы определения бинов](#5-%D0%9A%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D1%83%D1%80%D0%B0%D1%86%D0%B8%D0%B8-%D1%81%D0%BF%D0%BE%D1%81%D0%BE%D0%B1%D1%8B-%D0%BE%D0%BF%D1%80%D0%B5%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F-%D0%B1%D0%B8%D0%BD%D0%BE%D0%B2)
- [4. Базы данных (JDBC, JPA, Hibernate)](#4-%D0%91%D0%B0%D0%B7%D1%8B-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85-jdbc-jpa-hibernate)
		- [1. JDBC API: создание соединений, выполнение запросов](#1-jdbc-api-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D1%81%D0%BE%D0%B5%D0%B4%D0%B8%D0%BD%D0%B5%D0%BD%D0%B8%D0%B9-%D0%B2%D1%8B%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D0%BE%D0%B2)
		- [2. Базовые операции JPA: аннотации `@Entity`, `@Table`, `@Id`](#2-%D0%91%D0%B0%D0%B7%D0%BE%D0%B2%D1%8B%D0%B5-%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8-jpa-%D0%B0%D0%BD%D0%BD%D0%BE%D1%82%D0%B0%D1%86%D0%B8%D0%B8-entity-table-id)
		- [3. Структура и конфигурация Hibernate: свойства и конфигурационные файлы](#3-%D0%A1%D1%82%D1%80%D1%83%D0%BA%D1%82%D1%83%D1%80%D0%B0-%D0%B8-%D0%BA%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D1%83%D1%80%D0%B0%D1%86%D0%B8%D1%8F-hibernate-%D1%81%D0%B2%D0%BE%D0%B9%D1%81%D1%82%D0%B2%D0%B0-%D0%B8-%D0%BA%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D1%83%D1%80%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D1%8B%D0%B5-%D1%84%D0%B0%D0%B9%D0%BB%D1%8B)
		- [4. Ассоциации в Hibernate: `OneToMany`, `ManyToMany`](#4-%D0%90%D1%81%D1%81%D0%BE%D1%86%D0%B8%D0%B0%D1%86%D0%B8%D0%B8-%D0%B2-hibernate-onetomany-manytomany)
		- [5. Транзакции: управление транзакциями в JPA и Hibernate, аннотация `@Transactional`](#5-%D0%A2%D1%80%D0%B0%D0%BD%D0%B7%D0%B0%D0%BA%D1%86%D0%B8%D0%B8-%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D1%82%D1%80%D0%B0%D0%BD%D0%B7%D0%B0%D0%BA%D1%86%D0%B8%D1%8F%D0%BC%D0%B8-%D0%B2-jpa-%D0%B8-hibernate-%D0%B0%D0%BD%D0%BD%D0%BE%D1%82%D0%B0%D1%86%D0%B8%D1%8F-transactional)
- [5. Spring MVC](#5-spring-mvc)
		- [1. Архитектура MVC: концепции, разделение на модель, представление, контроллер](#1-%D0%90%D1%80%D1%85%D0%B8%D1%82%D0%B5%D0%BA%D1%82%D1%83%D1%80%D0%B0-mvc-%D0%BA%D0%BE%D0%BD%D1%86%D0%B5%D0%BF%D1%86%D0%B8%D0%B8-%D1%80%D0%B0%D0%B7%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BD%D0%B0-%D0%BC%D0%BE%D0%B4%D0%B5%D0%BB%D1%8C-%D0%BF%D1%80%D0%B5%D0%B4%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D0%BB%D0%B5%D1%80)
		- [2. Контроллеры: аннотации `@Controller`, `@RequestMapping`, обработка форм](#2-%D0%9A%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D0%BB%D0%B5%D1%80%D1%8B-%D0%B0%D0%BD%D0%BD%D0%BE%D1%82%D0%B0%D1%86%D0%B8%D0%B8-controller-requestmapping-%D0%BE%D0%B1%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0-%D1%84%D0%BE%D1%80%D0%BC)
		- [3. Модель и представление: передача данных между контроллером и представлением](#3-%D0%9C%D0%BE%D0%B4%D0%B5%D0%BB%D1%8C-%D0%B8-%D0%BF%D1%80%D0%B5%D0%B4%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BF%D0%B5%D1%80%D0%B5%D0%B4%D0%B0%D1%87%D0%B0-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85-%D0%BC%D0%B5%D0%B6%D0%B4%D1%83-%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D0%BB%D0%B5%D1%80%D0%BE%D0%BC-%D0%B8-%D0%BF%D1%80%D0%B5%D0%B4%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5%D0%BC)
		- [4. Связывание параметров: аннотации `@RequestParam`, `@PathVariable`, `@ModelAttribute`](#4-%D0%A1%D0%B2%D1%8F%D0%B7%D1%8B%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D0%B0%D1%80%D0%B0%D0%BC%D0%B5%D1%82%D1%80%D0%BE%D0%B2-%D0%B0%D0%BD%D0%BD%D0%BE%D1%82%D0%B0%D1%86%D0%B8%D0%B8-requestparam-pathvariable-modelattribute)
- [6. Rest, Rest Api](#6-rest-rest-api)
		- [1. Принципы REST: статусы HTTP, методы HTTP](#1-%D0%9F%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF%D1%8B-rest-%D1%81%D1%82%D0%B0%D1%82%D1%83%D1%81%D1%8B-http-%D0%BC%D0%B5%D1%82%D0%BE%D0%B4%D1%8B-http)
		- [2. Создание REST-контроллеров: `@RestController`, `@RequestMapping`](#2-%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-rest-%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D0%BB%D0%B5%D1%80%D0%BE%D0%B2-restcontroller-requestmapping)
		- [3. Форматы данных: возвращение JSON и XML с Jackson](#3-%D0%A4%D0%BE%D1%80%D0%BC%D0%B0%D1%82%D1%8B-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85-%D0%B2%D0%BE%D0%B7%D0%B2%D1%80%D0%B0%D1%89%D0%B5%D0%BD%D0%B8%D0%B5-json-%D0%B8-xml-%D1%81-jackson)
		- [4. Spring RestTemplate и WebClient: взаимодействие с REST API](#4-spring-resttemplate-%D0%B8-webclient-%D0%B2%D0%B7%D0%B0%D0%B8%D0%BC%D0%BE%D0%B4%D0%B5%D0%B9%D1%81%D1%82%D0%B2%D0%B8%D0%B5-%D1%81-rest-api)
- [7. Boot, Data, Security](#7-boot-data-security)
		- [1. Spring Boot: создание проекта, авто-конфигурация](#1-spring-boot-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0-%D0%B0%D0%B2%D1%82%D0%BE-%D0%BA%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D1%83%D1%80%D0%B0%D1%86%D0%B8%D1%8F)
		- [2. Стартеры: использование зависимостей Spring Boot](#2-%D0%A1%D1%82%D0%B0%D1%80%D1%82%D0%B5%D1%80%D1%8B-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B7%D0%B0%D0%B2%D0%B8%D1%81%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B5%D0%B9-spring-boot)
		- [3. Spring Data JPA: интерфейс `CrudRepository`, `JpaRepository`](#3-spring-data-jpa-%D0%B8%D0%BD%D1%82%D0%B5%D1%80%D1%84%D0%B5%D0%B9%D1%81-crudrepository-jparepository)
		- [4. Запросы на основе методов: написание репозиториев с пользовательскими запросами](#4-%D0%97%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D1%8B-%D0%BD%D0%B0-%D0%BE%D1%81%D0%BD%D0%BE%D0%B2%D0%B5-%D0%BC%D0%B5%D1%82%D0%BE%D0%B4%D0%BE%D0%B2-%D0%BD%D0%B0%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B5%D0%B2-%D1%81-%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D1%81%D0%BA%D0%B8%D0%BC%D0%B8-%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D0%B0%D0%BC%D0%B8)
		- [5. Spring Security: настройка аутентификации и авторизации, роли](#5-spring-security-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%B0%D1%83%D1%82%D0%B5%D0%BD%D1%82%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D0%B8-%D0%B8-%D0%B0%D0%B2%D1%82%D0%BE%D1%80%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D0%B8-%D1%80%D0%BE%D0%BB%D0%B8)
		- [6. Настройка прав доступа: аннотации `@Secured`, `@PreAuthorize`](#6-%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%BF%D1%80%D0%B0%D0%B2-%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0-%D0%B0%D0%BD%D0%BD%D0%BE%D1%82%D0%B0%D1%86%D0%B8%D0%B8-secured-preauthorize)
- [8. Тестирование (JUnit, Mockito)](#8-%D0%A2%D0%B5%D1%81%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-junit-mockito)
		- [1. JUnit 5: написание тестовых классов, аннотации `@Test`, `@BeforeEach`, `@AfterEach`](#1-junit-5-%D0%BD%D0%B0%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D1%82%D0%B5%D1%81%D1%82%D0%BE%D0%B2%D1%8B%D1%85-%D0%BA%D0%BB%D0%B0%D1%81%D1%81%D0%BE%D0%B2-%D0%B0%D0%BD%D0%BD%D0%BE%D1%82%D0%B0%D1%86%D0%B8%D0%B8-test-beforeeach-aftereach)
		- [2. Сценарии тестирования: параметризованные и повторяющиеся тесты](#2-%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B8-%D1%82%D0%B5%D1%81%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F-%D0%BF%D0%B0%D1%80%D0%B0%D0%BC%D0%B5%D1%82%D1%80%D0%B8%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D1%8B%D0%B5-%D0%B8-%D0%BF%D0%BE%D0%B2%D1%82%D0%BE%D1%80%D1%8F%D1%8E%D1%89%D0%B8%D0%B5%D1%81%D1%8F-%D1%82%D0%B5%D1%81%D1%82%D1%8B)
		- [3. Mockito: создание моков (mock объектов), настройки поведения моков](#3-mockito-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BC%D0%BE%D0%BA%D0%BE%D0%B2-mock-%D0%BE%D0%B1%D1%8A%D0%B5%D0%BA%D1%82%D0%BE%D0%B2-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B8-%D0%BF%D0%BE%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D1%8F-%D0%BC%D0%BE%D0%BA%D0%BE%D0%B2)
		- [4. Внедрение моков: использование аннотаций `@Mock`, `@InjectMocks`](#4-%D0%92%D0%BD%D0%B5%D0%B4%D1%80%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BC%D0%BE%D0%BA%D0%BE%D0%B2-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B0%D0%BD%D0%BD%D0%BE%D1%82%D0%B0%D1%86%D0%B8%D0%B9-mock-injectmocks)
		- [5. Тестирование исключений: проверка выброса исключений в JUnit](#5-%D0%A2%D0%B5%D1%81%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B8%D1%81%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B9-%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0-%D0%B2%D1%8B%D0%B1%D1%80%D0%BE%D1%81%D0%B0-%D0%B8%D1%81%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B9-%D0%B2-junit)

# 1. Многопоточность
### 1. Создание потоков: использование `Thread` и `Runnable`
В Java есть два основных способа создания потоков: наследование от класса `Thread` и реализация интерфейса `Runnable`.

**Наследование от `Thread`:**
```
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running");
    }
    
    public static void main(String[] args) {
        MyThread thread = new MyThread();
        thread.start(); // Запуск потока
    }
}
```
Реализация интерфейса `Runnable`:
```
class MyRunnable implements Runnable {
    public void run() {
        System.out.println("Runnable is running");
    }

    public static void main(String[] args) {
        MyRunnable runnable = new MyRunnable();
        Thread thread = new Thread(runnable);
        thread.start(); // Запуск потока
    }
}
```
Второй способ предпочтительнее, так как Java не поддерживает множественное наследование классов, а интерфейсов может быть несколько.
### 2. Расширенные возможности потоков: использование `Callable` и `Future`

Интерфейс `Callable` аналогичен `Runnable`, но может возвращать результат и бросать исключения.

**Пример использования `Callable` и `Future`:**
```
import java.util.concurrent.Callable;
import java.util.concurrent.ExecutionException;
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;
import java.util.concurrent.Future;

public class CallableExample {
    public static void main(String[] args) {
        ExecutorService executor = Executors.newFixedThreadPool(1);
        
        Callable<Integer> task = () -> {
            Thread.sleep(1000);
            return 123;
        };

        Future<Integer> future = executor.submit(task);
        
        try {
            System.out.println("Future result: " + future.get()); // Ожидание завершения и получение результата
        } catch (InterruptedException | ExecutionException e) {
            e.printStackTrace();
        } finally {
            executor.shutdown();
        }
    }
}
```
### 3. Синхронизация: ключевое слово `synchronized`, проблемы гонки и deadlock

**Ключевое слово `synchronized`** предоставляет встроенные средства для синхронизации в Java и может использоваться для синхронизации методов или блоков кода.

#### Примеры использования:
- **Синхронизированный метод:**
```
public synchronized void method() {
    // Код синхронизирован
}
```
- **Синхронизированный блок:**
```
public void method() {
    synchronized(this) {
        // Код синхронизирован
    }
}
```
#### Основные характеристики:
1. **Простота использования:** Использовать `synchronized` очень просто, оно встроено в язык Java.
2. **Блокировка на уровне объекта:** Синхронизация осуществляется на уровне объекта или класса.
3. **Не поддерживает политику блокировок:** `synchronized` не предоставляет возможности попытки захвата блокировки (try-lock) или справедливой блокировки.
4. **Автоматическое управление блокировкой:** `synchronized` автоматически управляет блокировкой и разблокировкой (release) при входе и выходе из синхронизированного блока.

Пример `synchronized`:
```
class Counter {
    private int count = 0;

    public synchronized void increment() {
        count++;
    }

    public int getCount() {
        return count;
    }
}

public class SynchronizedExample {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();

        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();

        t1.join();
        t2.join();

        System.out.println("Final count: " + counter.getCount());
    }
}
```
**Проблемы гонки (race conditions):** Гонка возникает, когда два или более потоков пытаются изменить общий ресурс одновременно, что может привести к непредсказуемым результатам.

**Deadlock (взаимная блокировка):** Deadlock возникает, когда два или более потоков навсегда блокируются, ожидая друг друга.
### 4. Locks: использование `Lock`, `ReentrantLock`

**`ReentrantLock`** — это класс из пакета `java.util.concurrent.locks`, который предоставляет более гибкие и расширенные возможности по сравнению с `synchronized`.
#### Примеры использования:
- **Создание и использование `ReentrantLock`:**
```
import java.util.concurrent.locks.ReentrantLock;

public class MyClass {
    private final ReentrantLock lock = new ReentrantLock();

    public void method() {
        lock.lock();
        try {
            // Код синхронизирован
        } finally {
            lock.unlock();
        }
    }
}
```
#### Основные характеристики:
1. **Гибкость управления блокировкой:**
    - Позволяет явно захватывать и освобождать блокировку.
    - Поддерживает методы `lock()` и `unlock()` для явного управления блокировкой.
    - Метод `tryLock()` позволяет попытаться захватить блокировку без ожидания.
```
if (lock.tryLock()) {
    try {
        // Код синхронизирован
    } finally {
        lock.unlock();
    }
} else {
    // Не удалось захватить блокировку
}
```
2. **Политика справедливости:**
    - Поддерживает справедливые блокировки, где блокировки передаются потокам в порядке ожидания.
```
ReentrantLock fairLock = new ReentrantLock(true);
```
3. **Возможность прерывания блокировки:**
- Поддерживает метод `lockInterruptibly()`, который позволяет потокам прерываться, пока они ожидают захвата блокировки.
```
try {
    lock.lockInterruptibly();
    try {
        // Код синхронизирован
    } finally {
        lock.unlock();
    }
} catch (InterruptedException e) {
    // Поток был прерван
}
```
4. **Диагностика и мониторинг:**
- `ReentrantLock` предоставляет методы для проверки состояния блокировки, такие как `isLocked()`, `isHeldByCurrentThread()`, и `getHoldCount()`.

**Пример использования `ReentrantLock`:**
```
import java.util.concurrent.locks.Lock;
import java.util.concurrent.locks.ReentrantLock;

class Counter {
    private int count = 0;
    private final Lock lock = new ReentrantLock();

    public void increment() {
        lock.lock();
        try {
            count++;
        } finally {
            lock.unlock();
        }
    }

    public int getCount() {
        return count;
    }
}

public class LockExample {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();

        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();

        t1.join();
        t2.join();

        System.out.println("Final count: " + counter.getCount());
    }
}
```
### 5. Высокоуровневые конструкции: `ExecutorService`

`ExecutorService` упрощает управление пулом потоков и их жизненным циклом.

**Пример использования `ExecutorService`:**
```
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

public class ExecutorServiceExample {
    public static void main(String[] args) {
        ExecutorService executor = Executors.newFixedThreadPool(2);

        Runnable task1 = () -> {
            System.out.println("Task 1 is running");
        };

        Runnable task2 = () -> {
            System.out.println("Task 2 is running");
        };

        executor.submit(task1);
        executor.submit(task2);

        executor.shutdown();
    }
}
```
### 6. Конкурентные коллекции: `ConcurrentHashMap`, `CopyOnWriteArrayList`
#### Преимущества конкурентных коллекций:
1. **Потокобезопасность:**
	- **Обычные коллекции:** Не обеспечивают безопасный доступ из нескольких потоков. Если несколько потоков одновременно читают и изменяют коллекцию, это может привести к непредсказуемому поведению и ошибкам.
	- **Конкурентные коллекции:** Разработаны для безопасного доступа из нескольких потоков. Они используют различные механизмы синхронизации, такие как блокировки или немодифицируемые данные, для обеспечения корректности операций.
2. **Механизмы синхронизации:**
	- **Обычные коллекции:** Не используют синхронизацию, что делает их быстрыми для одиночного потока, но небезопасными для многопоточного использования.
	- **Конкурентные коллекции:** Используют различные механизмы, такие как внутренние блокировки (`ConcurrentHashMap`), копирование на запись (`CopyOnWriteArrayList`), блокирующие очереди (`BlockingQueue`), чтобы обеспечить корректность работы в многопоточной среде.

**ConcurrentHashMap:**
- Предоставляет потокобезопасную реализацию хеш-таблицы.
- Использует сегментацию, чтобы снизить количество блокировок при модификации карты.

Пример:
```
import java.util.concurrent.ConcurrentHashMap;

public class ConcurrentHashMapExample {
    public static void main(String[] args) {
        ConcurrentHashMap<String, String> map = new ConcurrentHashMap<>();
        map.put("key1", "value1");
        map.put("key2", "value2");

        System.out.println("Value for key1: " + map.get("key1"));
    }
}
```

**CopyOnWriteArrayList**:
- Реализация списка, в которой операции изменения (добавление, удаление) создают копию списка.
- Подходит для ситуаций, где чтения преобладают над записями.

Пример:
```
import java.util.List;
import java.util.concurrent.CopyOnWriteArrayList;

public class CopyOnWriteArrayListExample {
    public static void main(String[] args) {
        List<String> list = new CopyOnWriteArrayList<>();
        list.add("element1");
        list.add("element2");

        System.out.println("List: " + list);
    }
}
```
### Важные аспекты при работе с конкурентными коллекциями
1. **Производительность:**
    - Конкурентные коллекции часто имеют большую накладную стоимость из-за механизмов синхронизации.
    - Например, `CopyOnWriteArrayList` эффективен для сценариев, где чтения преобладают над изменениями, но может быть неэффективен для частых модификаций.
2. **Правильность использования:**
    - Несмотря на потокобезопасность, важно понимать, как коллекция синхронизирует операции.
    - Некоторые методы могут по-прежнему требовать внешней синхронизации для составных операций (например, несколько вызовов `get` и `put` в `ConcurrentHashMap`).
3. **Выбор коллекции:**
    - Выбор правильной коллекции зависит от конкретных требований и паттернов использования.
    - Например, `ConcurrentHashMap` подходит для частых чтений и записей, тогда как `CopyOnWriteArrayList` подходит для преобладающих чтений с редкими модификациями.
# 2. Системы сборки
Maven и Gradle помогают управлять зависимостями, автоматизировать сборку и тестирование проектов, а также упрощают работу с большими проектами.
### 1. Maven: конфигурация проекта в `pom.xml`, жизненный цикл сборки

Maven — это система управления проектами, основанная на POM (Project Object Model). Она используется для управления зависимостями, сборки и развертывания проектов.

**Конфигурация проекта в `pom.xml`:**
```
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <groupId>com.example</groupId>
    <artifactId>my-app</artifactId>
    <version>1.0-SNAPSHOT</version>
    <dependencies>
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>4.12</version>
            <scope>test</scope>
        </dependency>
    </dependencies>
</project>
```
Основные элементы `pom.xml`:

- `<groupId>`: уникальный идентификатор группы проекта.
- `<artifactId>`: уникальный идентификатор артефакта (проекта).
- `<version>`: версия проекта.
- `<dependencies>`: зависимости проекта.

**Жизненный цикл сборки:** Maven имеет три основных жизненных цикла сборки: `default`, `clean`, и `site`.

- `validate`: проверка корректности проекта.
- `compile`: компиляция исходного кода.
- `test`: выполнение тестов.
- `package`: упаковка проекта в формат JAR или WAR.
- `install`: установка пакета в локальный репозиторий.
- `deploy`: развертывание пакета в удаленный репозиторий.

### 2. Зависимости в Maven: управление иерархией зависимостей, репозитории

**Управление зависимостями:** Maven управляет зависимостями через центральный репозиторий Maven и позволяет определять зависимости в `pom.xml`.

**Пример иерархии зависимостей:**
```
<dependencies>
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-core</artifactId>
        <version>5.3.8</version>
    </dependency>
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-context</artifactId>
        <version>5.3.8</version>
    </dependency>
</dependencies>
```
Maven автоматически разрешает транзитивные зависимости, т.е. зависимости зависимостей.

**Репозитории:**

- **Локальный репозиторий**: хранится на локальной машине (обычно в `~/.m2/repository`).
- **Центральный репозиторий**: публичный репозиторий Maven.
- **Удаленные репозитории**: определяются в `pom.xml` или в настройках Maven.
### 3. Gradle: написание `build.gradle` скриптов

Gradle — это система автоматизации сборки, использующая язык Groovy или Kotlin для написания скриптов сборки.

**Пример `build.gradle`:**
```
plugins {
    id 'java'
}

group 'com.example'
version '1.0-SNAPSHOT'

repositories {
    mavenCentral()
}

dependencies {
    testImplementation 'junit:junit:4.12'
}
```
Основные элементы `build.gradle`:

- `plugins`: плагины, используемые в проекте.
- `group`: идентификатор группы проекта.
- `version`: версия проекта.
- `repositories`: репозитории для поиска зависимостей.
- `dependencies`: зависимости проекта.

### 4. Задачи в Gradle: создание и запуск пользовательских задач

Gradle позволяет создавать пользовательские задачи для автоматизации различных этапов сборки.

**Пример пользовательской задачи:**
```
task hello {
    doLast {
        println 'Hello, Gradle!'
    }
}
```
Для запуска задачи выполните команду `gradle hello`.

**Создание задач с зависимостями:**
```
task taskA {
    doLast {
        println 'Task A'
    }
}

task taskB(dependsOn: taskA) {
    doLast {
        println 'Task B'
    }
}
```
В этом примере `taskB` будет выполнена после `taskA`.

### 5. Плагины: использование и конфигурация плагинов в Maven и Gradle

**Плагины в Maven:** Плагины добавляются в секцию `<build>` файла `pom.xml`.

**Пример использования плагина:**
```
<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-compiler-plugin</artifactId>
            <version>3.8.1</version>
            <configuration>
                <source>1.8</source>
                <target>1.8</target>
            </configuration>
        </plugin>
    </plugins>
</build>
```
Этот пример показывает конфигурацию плагина компилятора Maven.

**Плагины в Gradle:** Плагины добавляются в секцию `plugins` файла `build.gradle`.

**Пример использования плагина:**
```
plugins {
    id 'java'
    id 'application'
}

application {
    mainClassName = 'com.example.Main'
}
```
Этот пример показывает использование плагинов `java` и `application` в Gradle.
# 3. IoC и DI (Inversion of Control и Dependency Injection)
### 1. Основы IoC: принципы инверсии управления

**Inversion of Control (IoC)** — это принцип, при котором управление объектами или компонентами передается контейнеру или фреймворку. Это означает, что вместо того, чтобы объекты сами создавали свои зависимости, они получают эти зависимости извне.

**Основные принципы IoC:**
- **Контейнер управления:** Контейнер IoC отвечает за создание и управление жизненным циклом объектов.
- **Инъекция зависимостей:** Контейнер IoC передает зависимости объектам, снижая связанность компонентов и повышая модульность и тестируемость кода.

### 2. Типы DI: конструкторная, сеттерная, интерфейсная инъекции

**Конструкторная инъекция:** Передача зависимостей через конструктор объекта.
```
public class Service {
    private Repository repository;

    public Service(Repository repository) {
        this.repository = repository;
    }
}
```
**Сеттерная инъекция:** Передача зависимостей через сеттер-методы.
```
public class Service {
    private Repository repository;

    public void setRepository(Repository repository) {
        this.repository = repository;
    }
}
```
**Интерфейсная инъекция:** Передача зависимостей через методы интерфейса. Этот подход используется реже.
```
public interface Service {
    void setRepository(Repository repository);
}
```
### 3. Spring IoC контейнер: использование аннотаций `@Component`, `@Autowired`

**Spring IoC контейнер** предоставляет инфраструктуру для управления зависимостями и конфигурациями компонентов приложения.

**Аннотация `@Component`:** Используется для автоматического обнаружения и регистрации бина в Spring IoC контейнере.
```
import org.springframework.stereotype.Component;

@Component
public class Repository {
    // Реализация класса
}
```
**Аннотация `@Autowired`:** Используется для автоматической инъекции зависимостей.
```
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

@Service
public class Service {
    private final Repository repository;

    @Autowired
    public Service(Repository repository) {
        this.repository = repository;
    }
}
```
### 4. Singleton и Prototype: scoping биннов в Spring

**Scope биннов** определяет, как Spring создает и управляет экземплярами бинов.

**Singleton:** По умолчанию все бины в Spring являются синглтонами, что означает, что контейнер создает только один экземпляр каждого бина.
```
import org.springframework.context.annotation.Scope;
import org.springframework.stereotype.Component;

@Component
@Scope("singleton")
public class SingletonBean {
    // Реализация класса
}
```
**Prototype:** Для каждого запроса контейнер создает новый экземпляр бина.
```
import org.springframework.context.annotation.Scope;
import org.springframework.stereotype.Component;

@Component
@Scope("prototype")
public class PrototypeBean {
    // Реализация класса
}
```
### 5. Конфигурации: способы определения бинов

**Конфигурация с помощью аннотаций:** Использование аннотаций `@Component`, `@Service`, `@Repository` для автоматического сканирования компонентов.
```
import org.springframework.context.annotation.ComponentScan;
import org.springframework.context.annotation.Configuration;

@Configuration
@ComponentScan(basePackages = "com.example")
public class AppConfig {
    // Конфигурация приложения
}
```
**Конфигурация с помощью XML:** Использование XML-файлов для определения бинов.
```
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
       http://www.springframework.org/schema/beans/spring-beans.xsd">
    
    <bean id="service" class="com.example.Service">
        <property name="repository" ref="repository"/>
    </bean>
    
    <bean id="repository" class="com.example.Repository"/>
</beans>
```
**Конфигурация с помощью Java:** Использование класса конфигурации для определения бинов.
```
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

@Configuration
public class AppConfig {
    
    @Bean
    public Repository repository() {
        return new Repository();
    }

    @Bean
    public Service service() {
        return new Service(repository());
    }
}
```
# 4. Базы данных (JDBC, JPA, Hibernate)
### 1. JDBC API: создание соединений, выполнение запросов

**JDBC (Java Database Connectivity)** — это API, который позволяет Java-приложениям взаимодействовать с базами данных.

**Создание соединений:** Для создания соединения с базой данных используем класс `DriverManager`.
```
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

public class JDBCExample {
    public static void main(String[] args) {
        String url = "jdbc:mysql://localhost:3306/mydatabase";
        String user = "root";
        String password = "password";

        try (Connection connection = DriverManager.getConnection(url, user, password)) {
            if (connection != null) {
                System.out.println("Connected to the database!");
            } else {
                System.out.println("Failed to make connection!");
            }
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
}
```
**Выполнение запросов:** Используем интерфейсы `Statement` или `PreparedStatement` для выполнения SQL-запросов.
```
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.sql.SQLException;

public class JDBCQueryExample {
    public static void main(String[] args) {
        String url = "jdbc:mysql://localhost:3306/mydatabase";
        String user = "root";
        String password = "password";

        String query = "SELECT * FROM users WHERE id = ?";

        try (Connection connection = DriverManager.getConnection(url, user, password);
             PreparedStatement statement = connection.prepareStatement(query)) {
            statement.setInt(1, 1);
            ResultSet resultSet = statement.executeQuery();

            while (resultSet.next()) {
                System.out.println("User ID: " + resultSet.getInt("id"));
                System.out.println("User Name: " + resultSet.getString("name"));
            }
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
}
```
### 2. Базовые операции JPA: аннотации `@Entity`, `@Table`, `@Id`

**JPA (Java Persistence API)** — это стандарт для работы с объектно-реляционным маппингом (ORM).

**Аннотация `@Entity`:** Определяет класс как сущность.
```
import javax.persistence.Entity;
import javax.persistence.Id;

@Entity
public class User {
    @Id
    private int id;
    private String name;

    // Getters and setters
}
```
**Аннотация `@Table`:** Используется для указания имени таблицы.
```
import javax.persistence.Entity;
import javax.persistence.Id;
import javax.persistence.Table;

@Entity
@Table(name = "users")
public class User {
    @Id
    private int id;
    private String name;

    // Getters and setters
}
```
**Аннотация `@Id`:** Указывает первичный ключ сущности.
```
import javax.persistence.Entity;
import javax.persistence.Id;

@Entity
public class User {
    @Id
    private int id;
    private String name;

    // Getters and setters
}
```
### 3. Структура и конфигурация Hibernate: свойства и конфигурационные файлы

**Hibernate** — это популярная реализация JPA, которая обеспечивает ORM-возможности.

**Конфигурационный файл Hibernate (`hibernate.cfg.xml`):**
```
<!DOCTYPE hibernate-configuration PUBLIC "-//Hibernate/Hibernate Configuration DTD 3.0//EN"
                                         "http://hibernate.sourceforge.net/hibernate-configuration-3.0.dtd">
<hibernate-configuration>
    <session-factory>
        <property name="hibernate.dialect">org.hibernate.dialect.MySQLDialect</property>
        <property name="hibernate.connection.driver_class">com.mysql.jdbc.Driver</property>
        <property name="hibernate.connection.url">jdbc:mysql://localhost:3306/mydatabase</property>
        <property name="hibernate.connection.username">root</property>
        <property name="hibernate.connection.password">password</property>
        <property name="hibernate.hbm2ddl.auto">update</property>
        
        <mapping class="com.example.User"/>
    </session-factory>
</hibernate-configuration>
```
Конфигурация с использованием Java-класса:
```
import org.hibernate.SessionFactory;
import org.hibernate.cfg.Configuration;

public class HibernateUtil {
    private static final SessionFactory sessionFactory;

    static {
        try {
            sessionFactory = new Configuration().configure().buildSessionFactory();
        } catch (Throwable ex) {
            throw new ExceptionInInitializerError(ex);
        }
    }

    public static SessionFactory getSessionFactory() {
        return sessionFactory;
    }
}
```
### 4. Ассоциации в Hibernate: `OneToMany`, `ManyToMany`

**OneToMany:**
```
import javax.persistence.*;
import java.util.Set;

@Entity
public class Department {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String name;

    @OneToMany(mappedBy = "department")
    private Set<Employee> employees;

    // Getters and setters
}

@Entity
public class Employee {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String name;

    @ManyToOne
    @JoinColumn(name = "department_id")
    private Department department;

    // Getters and setters
}
```
ManyToMany:
```
import javax.persistence.*;
import java.util.Set;

@Entity
public class Project {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String name;

    @ManyToMany
    @JoinTable(
        name = "project_employee",
        joinColumns = @JoinColumn(name = "project_id"),
        inverseJoinColumns = @JoinColumn(name = "employee_id")
    )
    private Set<Employee> employees;

    // Getters and setters
}

@Entity
public class Employee {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String name;

    @ManyToMany(mappedBy = "employees")
    private Set<Project> projects;

    // Getters and setters
}
```
### 5. Транзакции: управление транзакциями в JPA и Hibernate, аннотация `@Transactional`

**Управление транзакциями с использованием JPA и Hibernate:**
```
import org.hibernate.Session;
import org.hibernate.Transaction;

public class HibernateTransactionExample {
    public static void main(String[] args) {
        Session session = HibernateUtil.getSessionFactory().openSession();
        Transaction transaction = null;

        try {
            transaction = session.beginTransaction();

            // Операции с базой данных
            Employee employee = new Employee();
            employee.setName("John Doe");
            session.save(employee);

            transaction.commit();
        } catch (Exception e) {
            if (transaction != null) {
                transaction.rollback();
            }
            e.printStackTrace();
        } finally {
            session.close();
        }
    }
}
```
**Аннотация `@Transactional`:** Используется для обозначения методов, которые должны выполняться в транзакции.
```
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

@Service
public class EmployeeService {
    
    @Transactional
    public void saveEmployee(Employee employee) {
        // Операции с базой данных
    }
}
```
# 5. Spring MVC
### 1. Архитектура MVC: концепции, разделение на модель, представление, контроллер

**Архитектура MVC (Model-View-Controller)** — это шаблон проектирования, который разделяет приложение на три основных компонента:

- **Модель (Model):** Содержит данные и бизнес-логику приложения.
- **Представление (View):** Отвечает за отображение данных пользователю.
- **Контроллер (Controller):** Обрабатывает пользовательский ввод и взаимодействует с моделью для обновления представления.

Это разделение позволяет достичь лучшей организованности кода и облегчает поддержку и тестирование приложения.

### 2. Контроллеры: аннотации `@Controller`, `@RequestMapping`, обработка форм

**Аннотация `@Controller`:** Обозначает класс как контроллер в Spring MVC.
```
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;

@Controller
public class HomeController {
    
    @RequestMapping("/")
    public String home() {
        return "home"; // Возвращает имя представления (home.jsp)
    }
}
```
**Аннотация `@RequestMapping`:** Используется для маппинга запросов к методам контроллера.
```
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestMethod;

@Controller
public class FormController {
    
    @RequestMapping(value = "/form", method = RequestMethod.GET)
    public String showForm() {
        return "form"; // Возвращает имя представления (form.jsp)
    }
    
    @RequestMapping(value = "/form", method = RequestMethod.POST)
    public String submitForm(@RequestParam("name") String name, Model model) {
        model.addAttribute("name", name);
        return "result"; // Возвращает имя представления (result.jsp)
    }
}
```
### 3. Модель и представление: передача данных между контроллером и представлением

**Передача данных через объект `Model`:** Контроллеры могут передавать данные в представление через объект `Model`.
```
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.RequestMapping;

@Controller
public class GreetingController {
    
    @RequestMapping("/greeting")
    public String greeting(Model model) {
        model.addAttribute("message", "Hello, World!");
        return "greeting"; // Возвращает имя представления (greeting.jsp)
    }
}
```
В представлении (например, `greeting.jsp`) можно отобразить переданные данные:
```
<html>
<body>
    <h1>${message}</h1>
</body>
</html>
```
### 4. Связывание параметров: аннотации `@RequestParam`, `@PathVariable`, `@ModelAttribute`

**Аннотация `@RequestParam`:** Используется для связывания параметров запроса с аргументами метода контроллера.
```
import org.springframework.web.bind.annotation.RequestParam;

@Controller
public class SearchController {
    
    @RequestMapping("/search")
    public String search(@RequestParam("query") String query, Model model) {
        model.addAttribute("query", query);
        return "searchResults"; // Возвращает имя представления (searchResults.jsp)
    }
}
```
**Аннотация `@PathVariable`:** Используется для извлечения значений из URI и связывания их с аргументами метода контроллера.
```
import org.springframework.web.bind.annotation.PathVariable;

@Controller
public class UserController {
    
    @RequestMapping("/user/{id}")
    public String getUser(@PathVariable("id") int userId, Model model) {
        // Предположим, что мы получили объект пользователя по его ID
        User user = userService.getUserById(userId);
        model.addAttribute("user", user);
        return "userProfile"; // Возвращает имя представления (userProfile.jsp)
    }
}
```
**Аннотация `@ModelAttribute`:** Используется для связывания данных формы с объектом модели и добавления этого объекта в модель.
```
import org.springframework.web.bind.annotation.ModelAttribute;

@Controller
public class RegistrationController {
    
    @RequestMapping(value = "/register", method = RequestMethod.GET)
    public String showRegistrationForm(Model model) {
        model.addAttribute("user", new User());
        return "registration"; // Возвращает имя представления (registration.jsp)
    }
    
    @RequestMapping(value = "/register", method = RequestMethod.POST)
    public String register(@ModelAttribute("user") User user, Model model) {
        // Логика сохранения пользователя
        userService.saveUser(user);
        model.addAttribute("message", "Registration successful");
        return "result"; // Возвращает имя представления (result.jsp)
    }
}
```
# 6. Rest, Rest Api
### 1. Принципы REST: статусы HTTP, методы HTTP

**REST (Representational State Transfer)** — это архитектурный стиль для создания веб-сервисов, использующий HTTP для выполнения операций с ресурсами.

#### Методы HTTP:

- **GET:** Получение ресурса.
- **POST:** Создание нового ресурса.
- **PUT:** Обновление существующего ресурса.
- **DELETE:** Удаление ресурса.
- **PATCH:** Частичное обновление ресурса.

#### Статусы HTTP:

- **200 OK:** Успешное выполнение запроса.
- **201 Created:** Ресурс успешно создан.
- **204 No Content:** Успешное выполнение запроса, но нет содержимого для возвращения.
- **400 Bad Request:** Некорректный запрос.
- **401 Unauthorized:** Требуется аутентификация.
- **403 Forbidden:** Доступ к ресурсу запрещен.
- **404 Not Found:** Ресурс не найден.
- **500 Internal Server Error:** Внутренняя ошибка сервера.

### 2. Создание REST-контроллеров: `@RestController`, `@RequestMapping`

**Аннотация `@RestController`:** Обозначает класс как REST-контроллер, объединяет `@Controller` и `@ResponseBody`, возвращая данные прямо в тело ответа.
```
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
@RequestMapping("/api/users")
public class UserController {

    @GetMapping("/{id}")
    public User getUser(@PathVariable Long id) {
        // Логика получения пользователя по ID
        return userService.getUserById(id);
    }

    @PostMapping
    public User createUser(@RequestBody User user) {
        // Логика создания нового пользователя
        return userService.saveUser(user);
    }
}
```
### 3. Форматы данных: возвращение JSON и XML с Jackson

**Возвращение JSON:** По умолчанию, Spring Boot использует библиотеку Jackson для сериализации объектов в JSON.
```
@RestController
@RequestMapping("/api/products")
public class ProductController {

    @GetMapping("/{id}")
    public Product getProduct(@PathVariable Long id) {
        return productService.getProductById(id);
    }
}
```
**Возвращение XML:** Для поддержки XML нужно добавить зависимость `jackson-dataformat-xml` в `pom.xml`.
```
<dependency>
    <groupId>com.fasterxml.jackson.dataformat</groupId>
    <artifactId>jackson-dataformat-xml</artifactId>
</dependency>
```
И настроить контроллер:
```
import com.fasterxml.jackson.dataformat.xml.annotation.JacksonXmlRootElement;

@JacksonXmlRootElement(localName = "Product")
public class Product {
    // поля, геттеры и сеттеры
}

@RestController
@RequestMapping("/api/products")
public class ProductController {

    @GetMapping(value = "/{id}", produces = { "application/json", "application/xml" })
    public Product getProduct(@PathVariable Long id) {
        return productService.getProductById(id);
    }
}
```
### 4. Spring RestTemplate и WebClient: взаимодействие с REST API

**RestTemplate:** Используется для взаимодействия с RESTful веб-сервисами.
```
import org.springframework.web.client.RestTemplate;
import org.springframework.http.ResponseEntity;

public class RestClient {

    private static final String BASE_URL = "https://api.example.com";

    public User getUserById(Long id) {
        RestTemplate restTemplate = new RestTemplate();
        ResponseEntity<User> response = restTemplate.getForEntity(BASE_URL + "/users/" + id, User.class);
        return response.getBody();
    }

    public User createUser(User user) {
        RestTemplate restTemplate = new RestTemplate();
        ResponseEntity<User> response = restTemplate.postForEntity(BASE_URL + "/users", user, User.class);
        return response.getBody();
    }
}
```
**WebClient:** Современный, асинхронный и неблокирующий клиент для взаимодействия с RESTful веб-сервисами.
```
import org.springframework.web.reactive.function.client.WebClient;
import reactor.core.publisher.Mono;

public class WebClientExample {

    private final WebClient webClient = WebClient.create("https://api.example.com");

    public Mono<User> getUserById(Long id) {
        return webClient.get()
                        .uri("/users/{id}", id)
                        .retrieve()
                        .bodyToMono(User.class);
    }

    public Mono<User> createUser(User user) {
        return webClient.post()
                        .uri("/users")
                        .bodyValue(user)
                        .retrieve()
                        .bodyToMono(User.class);
    }
}
```
# 7. Boot, Data, Security
### 1. Spring Boot: создание проекта, авто-конфигурация

**Spring Boot** — это фреймворк, который упрощает создание приложений на основе Spring, предлагая авто-конфигурацию и встроенный сервер.

#### Создание проекта:

1. **Spring Initializr:** Используйте [Spring Initializr](https://start.spring.io/) для создания проекта.
    
    - Выберите зависимости, такие как Spring Web, Spring Data JPA, H2 Database (для простоты), Spring Security и Spring Boot DevTools.
2. **Структура проекта:** После создания и загрузки проекта у вас будет следующая структура:
    
    - `src/main/java` — основное место для вашего кода.
    - `src/main/resources` — конфигурационные файлы и шаблоны.

#### Пример основного класса:
```
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class MyApplication {
    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }
}
```
### 2. Стартеры: использование зависимостей Spring Boot

**Стартеры** — это наборы зависимостей для упрощения конфигурации приложения. Пример `pom.xml` с популярными стартерами:
```
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-security</artifactId>
    </dependency>
    <dependency>
        <groupId>com.h2database</groupId>
        <artifactId>h2</artifactId>
    </dependency>
</dependencies>
```
### 3. Spring Data JPA: интерфейс `CrudRepository`, `JpaRepository`

**Spring Data JPA** упрощает работу с базами данных, предлагая репозитории для стандартных операций.

**Интерфейс `CrudRepository`:**
```
import org.springframework.data.repository.CrudRepository;

public interface UserRepository extends CrudRepository<User, Long> {
}
```
Интерфейс `JpaRepository`:
```
import org.springframework.data.jpa.repository.JpaRepository;

public interface UserRepository extends JpaRepository<User, Long> {
}
```
### 4. Запросы на основе методов: написание репозиториев с пользовательскими запросами

**Spring Data JPA** позволяет создавать методы репозиториев на основе имен методов.

Примеры пользовательских запросов:
```
import org.springframework.data.jpa.repository.JpaRepository;
import java.util.List;

public interface UserRepository extends JpaRepository<User, Long> {
    List<User> findByLastName(String lastName);
    User findByEmail(String email);
    List<User> findByAgeGreaterThan(int age);
}
```
### 5. Spring Security: настройка аутентификации и авторизации, роли

**Spring Security** предоставляет мощные средства для защиты приложений.

#### Конфигурация безопасности:
```
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.security.config.annotation.web.builders.HttpSecurity;
import org.springframework.security.config.annotation.web.configuration.EnableWebSecurity;
import org.springframework.security.core.userdetails.User;
import org.springframework.security.core.userdetails.UserDetailsService;
import org.springframework.security.provisioning.InMemoryUserDetailsManager;
import org.springframework.security.web.SecurityFilterChain;

@Configuration
@EnableWebSecurity
public class SecurityConfig {

    @Bean
    public UserDetailsService userDetailsService() {
        InMemoryUserDetailsManager manager = new InMemoryUserDetailsManager();
        manager.createUser(User.withDefaultPasswordEncoder()
                               .username("user")
                               .password("password")
                               .roles("USER")
                               .build());
        manager.createUser(User.withDefaultPasswordEncoder()
                               .username("admin")
                               .password("password")
                               .roles("ADMIN")
                               .build());
        return manager;
    }

    @Bean
    public SecurityFilterChain securityFilterChain(HttpSecurity http) throws Exception {
        http
            .authorizeRequests()
                .antMatchers("/admin/**").hasRole("ADMIN")
                .antMatchers("/user/**").hasAnyRole("USER", "ADMIN")
                .antMatchers("/").permitAll()
                .and()
            .formLogin()
                .and()
            .logout()
                .permitAll();
        return http.build();
    }
}
```
### 6. Настройка прав доступа: аннотации `@Secured`, `@PreAuthorize`

**Аннотация `@Secured`:** Ограничивает доступ к методам по ролям.
```
import org.springframework.security.access.annotation.Secured;
import org.springframework.stereotype.Service;

@Service
public class AdminService {

    @Secured("ROLE_ADMIN")
    public void performAdminTask() {
        // Логика, доступная только для администраторов
    }
}
```
**Аннотация `@PreAuthorize`:** Используется для более гибкого контроля доступа, поддерживает SpEL (Spring Expression Language).
```
import org.springframework.security.access.prepost.PreAuthorize;
import org.springframework.stereotype.Service;

@Service
public class UserService {

    @PreAuthorize("hasRole('ROLE_USER') and #userId == authentication.principal.id")
    public User getUserDetails(Long userId) {
        // Логика, доступная для пользователя с определенным ID
        return userRepository.findById(userId).orElseThrow(() -> new UserNotFoundException(userId));
    }
}
```
# 8. Тестирование (JUnit, Mockito)
### 1. JUnit 5: написание тестовых классов, аннотации `@Test`, `@BeforeEach`, `@AfterEach`

**JUnit 5** — это популярный фреймворк для тестирования на Java.

#### Написание тестовых классов и использование аннотаций:
```
import org.junit.jupiter.api.*;

public class MyServiceTest {

    private MyService myService;

    @BeforeEach
    void setUp() {
        myService = new MyService();
    }

    @AfterEach
    void tearDown() {
        myService = null;
    }

    @Test
    void testMethod() {
        int result = myService.add(2, 3);
        Assertions.assertEquals(5, result, "2 + 3 should equal 5");
    }
}
```
- **`@Test`** — обозначает метод как тестовый.
- **`@BeforeEach`** — метод выполняется перед каждым тестовым методом.
- **`@AfterEach`** — метод выполняется после каждого тестового метода.

### 2. Сценарии тестирования: параметризованные и повторяющиеся тесты

#### Параметризованные тесты:
Позволяют запускать один и тот же тест с разными входными данными.
```
import org.junit.jupiter.params.ParameterizedTest;
import org.junit.jupiter.params.provider.ValueSource;

public class ParameterizedTestExample {

    @ParameterizedTest
    @ValueSource(ints = { 1, 2, 3, 4, 5 })
    void testWithDifferentValues(int number) {
        Assertions.assertTrue(number > 0 && number < 6);
    }
}
```
#### Повторяющиеся тесты:
Запускают один и тот же тест несколько раз.
```
import org.junit.jupiter.api.RepeatedTest;

public class RepeatedTestExample {

    @RepeatedTest(5)
    void repeatedTest() {
        // Тест будет выполнен 5 раз
        Assertions.assertTrue(Math.random() > 0);
    }
}
```
### 3. Mockito: создание моков (mock объектов), настройки поведения моков

**Mockito** — это библиотека для создания mock объектов и настройки их поведения в тестах.

#### Создание mock объектов и настройка поведения:
```
import static org.mockito.Mockito.*;
import org.mockito.Mockito;

public class MockitoExampleTest {

    @Test
    void testMock() {
        List<String> mockedList = Mockito.mock(List.class);

        when(mockedList.get(0)).thenReturn("first");
        when(mockedList.get(1)).thenReturn("second");

        Assertions.assertEquals("first", mockedList.get(0));
        Assertions.assertEquals("second", mockedList.get(1));
    }
}
```
### 4. Внедрение моков: использование аннотаций `@Mock`, `@InjectMocks`

#### Использование аннотаций `@Mock` и `@InjectMocks`:
```
import static org.mockito.Mockito.*;
import org.mockito.InjectMocks;
import org.mockito.Mock;
import org.mockito.MockitoAnnotations;
import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

public class MockitoInjectionTest {

    @Mock
    private Dependency dependency;

    @InjectMocks
    private Service service;

    @BeforeEach
    void setUp() {
        MockitoAnnotations.openMocks(this);
    }

    @Test
    void testServiceMethod() {
        when(dependency.someMethod()).thenReturn("mocked result");

        String result = service.useDependency();
        Assertions.assertEquals("mocked result", result);
    }
}
```
### 5. Тестирование исключений: проверка выброса исключений в JUnit

#### Проверка выброса исключений:
```
import org.junit.jupiter.api.Test;
import org.junit.jupiter.api.function.Executable;

public class ExceptionTest {

    @Test
    void testException() {
        Executable executable = () -> {
            throw new IllegalArgumentException("error message");
        };

        Assertions.assertThrows(IllegalArgumentException.class, executable);
    }
}
```