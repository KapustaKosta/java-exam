- [1. Многопоточность](#1-%D0%9C%D0%BD%D0%BE%D0%B3%D0%BE%D0%BF%D0%BE%D1%82%D0%BE%D1%87%D0%BD%D0%BE%D1%81%D1%82%D1%8C)
		- [1. Создание потоков: использование `Thread` и `Runnable`](#1-%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%B2-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-thread-%D0%B8-runnable)
		- [2. Расширенные возможности потоков: использование `Callable` и `Future`](#2-%D0%A0%D0%B0%D1%81%D1%88%D0%B8%D1%80%D0%B5%D0%BD%D0%BD%D1%8B%D0%B5-%D0%B2%D0%BE%D0%B7%D0%BC%D0%BE%D0%B6%D0%BD%D0%BE%D1%81%D1%82%D0%B8-%D0%BF%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%B2-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-callable-%D0%B8-future)
		- [3. Синхронизация: ключевое слово `synchronized`, проблемы гонки и deadlock](#3-%D0%A1%D0%B8%D0%BD%D1%85%D1%80%D0%BE%D0%BD%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F-%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%B2%D0%BE%D0%B5-%D1%81%D0%BB%D0%BE%D0%B2%D0%BE-synchronized-%D0%BF%D1%80%D0%BE%D0%B1%D0%BB%D0%B5%D0%BC%D1%8B-%D0%B3%D0%BE%D0%BD%D0%BA%D0%B8-%D0%B8-deadlock)
		- [4. Locks: использование `Lock`, `ReentrantLock`](#4-locks-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-lock-reentrantlock)
		- [5. Высокоуровневые конструкции: `ExecutorService`](#5-%D0%92%D1%8B%D1%81%D0%BE%D0%BA%D0%BE%D1%83%D1%80%D0%BE%D0%B2%D0%BD%D0%B5%D0%B2%D1%8B%D0%B5-%D0%BA%D0%BE%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%86%D0%B8%D0%B8-executorservice)
		- [6. Конкурентные коллекции: `ConcurrentHashMap`, `CopyOnWriteArrayList`](#6-%D0%9A%D0%BE%D0%BD%D0%BA%D1%83%D1%80%D0%B5%D0%BD%D1%82%D0%BD%D1%8B%D0%B5-%D0%BA%D0%BE%D0%BB%D0%BB%D0%B5%D0%BA%D1%86%D0%B8%D0%B8-concurrenthashmap-copyonwritearraylist)
		- [Важные аспекты при работе с конкурентными коллекциями](#%D0%92%D0%B0%D0%B6%D0%BD%D1%8B%D0%B5-%D0%B0%D1%81%D0%BF%D0%B5%D0%BA%D1%82%D1%8B-%D0%BF%D1%80%D0%B8-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B5-%D1%81-%D0%BA%D0%BE%D0%BD%D0%BA%D1%83%D1%80%D0%B5%D0%BD%D1%82%D0%BD%D1%8B%D0%BC%D0%B8-%D0%BA%D0%BE%D0%BB%D0%BB%D0%B5%D0%BA%D1%86%D0%B8%D1%8F%D0%BC%D0%B8)
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

**Объектно-реляционный маппинг (ORM)** — это технология, позволяющая преобразовывать данные между несовместимыми типами систем, таких как объектно-ориентированные языки программирования и реляционные базы данных. ORM предоставляет способ работы с данными базы данных в виде объектов, что упрощает процесс разработки и управления данными.
ORM автоматически генерирует SQL-запросы для создания, чтения, обновления и удаления данных.

1. Маппинг (соответствие) объектов и таблиц:**
    - В ORM классы в объектно-ориентированном языке программирования соответствуют таблицам в реляционной базе данных.
    - Объекты этих классов соответствуют строкам таблиц.
2. **Аннотации или XML-конфигурации:**
    - Для определения соответствия между классами и таблицами используются аннотации или XML-конфигурации.

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
#### One-to-Many (один-ко-многим)
**Отношение один-ко-многим** подразумевает, что одна сущность может быть связана с несколькими другими сущностями, но каждая из этих других сущностей связана только с одной сущностью.
#### Пример:
- Один пользователь (User) может иметь много заказов (Order).
- Один заказ (Order) принадлежит только одному пользователю (User).
```
@Entity
@Table(name = "users")
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @Column(name = "username")
    private String username;

    @OneToMany(mappedBy = "user", cascade = CascadeType.ALL, fetch = FetchType.LAZY)
    private List<Order> orders = new ArrayList<>();

    // Геттеры и сеттеры
}

@Entity
@Table(name = "orders")
public class Order {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @Column(name = "order_date")
    private LocalDate orderDate;

    @ManyToOne
    @JoinColumn(name = "user_id")
    private User user;

    // Геттеры и сеттеры
}
```
#### Характеристики:
- **`@OneToMany` аннотация:** Указывается на стороне "один".
- **`@ManyToOne` аннотация:** Указывается на стороне "много".
- **mappedBy:** Указывает, что отношение управляется полем `user` в классе `Order`.
- **cascade:** Определяет каскадирование операций (например, сохранение, удаление).
- **fetch:** Определяет стратегию загрузки (ленивую или жадную).

#### Many-to-Many (многие-ко-многим)
**Отношение многие-ко-многим** подразумевает, что каждая сущность может быть связана с несколькими другими сущностями, и каждая из этих других сущностей может быть связана с несколькими сущностями.

##### Пример:
- Один студент (Student) может быть записан на несколько курсов (Course).
- Один курс (Course) может включать нескольких студентов (Student).
```
@Entity
@Table(name = "students")
public class Student {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @Column(name = "name")
    private String name;

    @ManyToMany
    @JoinTable(
        name = "student_course",
        joinColumns = @JoinColumn(name = "student_id"),
        inverseJoinColumns = @JoinColumn(name = "course_id")
    )
    private List<Course> courses = new ArrayList<>();

    // Геттеры и сеттеры
}

@Entity
@Table(name = "courses")
public class Course {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @Column(name = "title")
    private String title;

    @ManyToMany(mappedBy = "courses")
    private List<Student> students = new ArrayList<>();

    // Геттеры и сеттеры
}
```
##### Характеристики:
- **`@ManyToMany` аннотация:** Указывается на обеих сторонах отношения.
- **`@JoinTable` аннотация:** Определяет таблицу соединения, которая связывает две сущности.
- **joinColumns:** Указывает на внешний ключ, ссылающийся на текущую сущность.
- **inverseJoinColumns:** Указывает на внешний ключ, ссылающийся на другую сущность.
- **mappedBy:** Указывает поле, управляющее отношением на другой стороне.

#### Сравнение One-to-Many и Many-to-Many

| Характеристика     | One-to-Many                             | Many-to-Many                  |
| ------------------ | --------------------------------------- | ----------------------------- |
| Отношение          | Один к многим                           | Многие ко многим              |
| Аннотация          | `@OneToMany` и `@ManyToOne`             | `@ManyToMany`                 |
| Стороны            | Указывается на стороне "один" и "много" | Указывается на обеих сторонах |
| Таблица соединения | Не требуется                            | Требуется для хранения связей |
| Пример             | Пользователь и заказы                   | Студенты и курсы              |
#### Важные аспекты при работе с отношениями
1. **Каскадирование:**
    - Определяет, какие операции (сохранение, обновление, удаление) должны каскадироваться от родительской сущности к дочерним.
    - Пример: `cascade = CascadeType.ALL`.
2. **Загрузка:**
    - Определяет, как сущности загружаются: лениво (LAZY) или жадно (EAGER).
    - Пример: `fetch = FetchType.LAZY`.
3. **mappedBy:**
    - Указывает, какая сторона управляет отношением и определяет собственность.
### 5. Транзакции: управление транзакциями в JPA и Hibernate, аннотация `@Transactional`

**Транзакции** — это механизм, который позволяет группировать несколько операций над базой данных в одно логическое целое. Транзакция гарантирует, что все операции внутри нее выполнятся успешно или ни одна из них не будет выполнена, если произойдет ошибка. Это обеспечивает согласованность данных и их целостность.

#### Основные свойства транзакций (ACID):
1. **Atomicity (Атомарность):** Все операции в транзакции либо завершаются успешно, либо не выполняются вообще.
2. **Consistency (Согласованность):** Транзакция переводит базу данных из одного согласованного состояния в другое.
3. **Isolation (Изоляция):** Результаты транзакции не видны другим параллельным транзакциям до её завершения.
4. **Durability (Устойчивость):** Изменения, внесенные транзакцией, сохраняются в базе данных даже в случае сбоя системы.

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
#### Декларативное управление транзакциями
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
#### Важные аспекты использования транзакций
1. **Propagation (Распространение):**
    - Определяет, как методы с аннотацией `@Transactional` должны вести себя в отношении уже существующих транзакций.
    - Примеры: `REQUIRED`, `REQUIRES_NEW`, `MANDATORY`.
2. **Isolation (Изоляция):**
    - Определяет уровень изоляции транзакции, что влияет на видимость изменений, сделанных другими параллельными транзакциями.
    - Примеры: `READ_COMMITTED`, `REPEATABLE_READ`, `SERIALIZABLE`.
3. **Rollback (Откат):**
    - Определяет, когда должна произойти отмена транзакции. Можно указать, какие исключения должны приводить к откату.
    - Пример: `@Transactional(rollbackFor = Exception.class)`.
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

`RestTemplate` и `WebClient` — это два различных клиента для выполнения HTTP-запросов в Spring. Они предоставляют возможности для взаимодействия с REST API, но имеют разные подходы и функциональные возможности.

#### RestTemplate

`RestTemplate` — это синхронный клиент для выполнения HTTP-запросов. Он был частью Spring Framework с ранних версий и стал стандартным способом взаимодействия с REST API до появления `WebClient`.

##### Особенности:
1. **Синхронность**: Все запросы выполняются в том же потоке, который их инициирует, что может привести к блокировке потоков при ожидании ответа.
2. **Удобство использования**: `RestTemplate` предоставляет удобные методы для отправки запросов и обработки ответов, например, `getForObject`, `postForEntity`, `exchange`.
3. **Поддержка Spring**: Легко интегрируется с остальными компонентами Spring.

##### Пример использования:
```
import org.springframework.web.client.RestTemplate;
import org.springframework.http.ResponseEntity;

public class RestTemplateExample {
    public static void main(String[] args) {
        RestTemplate restTemplate = new RestTemplate();
        String url = "https://api.example.com/data";

        // GET запрос
        ResponseEntity<String> response = restTemplate.getForEntity(url, String.class);
        System.out.println(response.getBody());
    }
}
```
#### WebClient
`WebClient` — это более современный и гибкий клиент, предоставляемый Spring WebFlux. Он поддерживает как синхронные, так и асинхронные запросы, что делает его более подходящим для высоконагруженных и реактивных приложений.

##### Особенности:
1. **Асинхронность**: Поддерживает асинхронное выполнение запросов, что позволяет не блокировать потоки и лучше использовать системные ресурсы.
2. **Реактивное программирование**: Основан на проекте Reactor и интегрируется с реактивным программированием.
3. **Гибкость**: Позволяет легко настраивать запросы и обработку ответов с использованием цепочек методов.
4. **Современные возможности**: Поддержка HTTP/2, веб-сокетов и других современных технологий.

##### Пример использования:
```
import org.springframework.web.reactive.function.client.WebClient;
import reactor.core.publisher.Mono;

public class WebClientExample {
    public static void main(String[] args) {
        WebClient webClient = WebClient.create("https://api.example.com");

        // Асинхронный GET запрос
        Mono<String> response = webClient.get()
                .uri("/data")
                .retrieve()
                .bodyToMono(String.class);

        // Подписка на результат
        response.subscribe(System.out::println);
    }
}
```
#### Сравнение `RestTemplate` и `WebClient`

| Характеристика          | RestTemplate                       | WebClient                             |
| ----------------------- | ---------------------------------- | ------------------------------------- |
| Синхронность            | Синхронный                         | Асинхронный и синхронный              |
| Реактивность            | Нет                                | Да                                    |
| Производительность      | Может блокировать потоки           | Неблокирующий, более производительный |
| Гибкость                | Ограниченная                       | Высокая гибкость и настройка          |
| Современные возможности | Нет                                | Поддержка HTTP/2, веб-сокетов и т.д.  |
| Поддержка в Spring      | Да                                 | Да                                    |
| Будущее развития        | Ограниченная поддержка, устаревший | Активное развитие и поддержка         |
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

`CrudRepository` и `JpaRepository` — это интерфейсы, предоставляемые Spring Data JPA для работы с базами данных. Они упрощают реализацию стандартных операций (CRUD — Create, Read, Update, Delete) и добавляют дополнительные возможности для работы с JPA.
**Spring Data JPA** упрощает работу с базами данных, предлагая репозитории для стандартных операций.

#### CrudRepository
`CrudRepository` — это базовый интерфейс, предоставляющий стандартные методы для выполнения CRUD-операций. Он является частью Spring Data и позволяет работать с сущностями без необходимости писать boilerplate-код для типичных операций.

##### Основные методы `CrudRepository`:
- `save(S entity)`: Сохраняет сущность.
- `saveAll(Iterable<S> entities)`: Сохраняет несколько сущностей.
- `findById(ID id)`: Находит сущность по её идентификатору.
- `existsById(ID id)`: Проверяет существование сущности по её идентификатору.
- `findAll()`: Возвращает все сущности.
- `findAllById(Iterable<ID> ids)`: Возвращает все сущности по их идентификаторам.
- `count()`: Возвращает количество сущностей.
- `deleteById(ID id)`: Удаляет сущность по её идентификатору.
- `delete(S entity)`: Удаляет сущность.
- `deleteAll(Iterable<? extends S> entities)`: Удаляет несколько сущностей.
- `deleteAll()`: Удаляет все сущности.

##### Пример использования `CrudRepository`:
```
import org.springframework.data.repository.CrudRepository;

public interface UserRepository extends CrudRepository<User, Long> {
    // Дополнительные методы можно определять здесь
}
```

#### JpaRepository
`JpaRepository` расширяет `CrudRepository` и добавляет дополнительные JPA-специфичные методы и функциональности. Он предоставляет более богатый набор операций, таких как пейджинг и сортировка, а также методы для выполнения сложных запросов.

##### Дополнительные методы `JpaRepository`:
- `findAll(Sort sort)`: Возвращает все сущности с учетом сортировки.
- `findAll(Pageable pageable)`: Возвращает страницы сущностей.
- `flush()`: Сбрасывает изменения в базу данных.
- `saveAndFlush(S entity)`: Сохраняет сущность и сразу сбрасывает изменения в базу данных.
- `deleteInBatch(Iterable<T> entities)`: Удаляет сущности в пакете.
- `deleteAllInBatch()`: Удаляет все сущности в пакете.
- И многие другие...

##### Пример использования `JpaRepository`:
```
import org.springframework.data.jpa.repository.JpaRepository;

public interface UserRepository extends JpaRepository<User, Long> {
    // Дополнительные методы можно определять здесь
}
```
#### Сравнение `CrudRepository` и `JpaRepository`

| Особенность            | CrudRepository                    | JpaRepository                        |
| ---------------------- | --------------------------------- | ------------------------------------ |
| Базовые CRUD операции  | Да                                | Да                                   |
| Пейджинг и сортировка  | Нет                               | Да                                   |
| JPA-специфичные методы | Нет                               | Да                                   |
| Поддержка транзакций   | Да (наследуется от JpaRepository) | Да                                   |
| Пример использования   | Простые CRUD операции             | Расширенные возможности работы с JPA |
#### Когда использовать
- **CrudRepository**: Если вам нужны только базовые CRUD операции без дополнительных возможностей пейджинга, сортировки и JPA-специфичных методов.
- **JpaRepository**: Если вам нужны дополнительные возможности, такие как пейджинг, сортировка и другие методы, специфичные для JPA. Этот интерфейс является более мощным и гибким по сравнению с `CrudRepository`.
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

`SecurityFilterChain` — это ключевой компонент в Spring Security, который отвечает за определение цепочки фильтров безопасности, применяемых к HTTP-запросам в приложении. Он позволяет конфигурировать правила доступа, аутентификации и авторизации для различных URL-адресов.

#### Основные компоненты и работа `SecurityFilterChain`
##### 1. **Фильтры безопасности**
- Фильтры являются основными строительными блоками в Spring Security, обрабатывающими запросы и применяющими к ним различные правила безопасности.
- Каждый фильтр выполняет конкретную задачу, такую как аутентификация, авторизация, обработка CORS и т.д.
- Фильтры могут быть связаны в цепочку, через которую проходят все запросы.
##### 2. **Конфигурация `SecurityFilterChain`**
- Конфигурация определяет, какие фильтры и в каком порядке будут применяться к запросам.
- Это можно настроить с помощью класса `SecurityConfigurerAdapter` или аннотации `@EnableWebSecurity` вместе с методами конфигурации.

#### Пример конфигурации `SecurityFilterChain`
```
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.security.config.annotation.web.builders.HttpSecurity;
import org.springframework.security.config.annotation.web.configuration.EnableWebSecurity;
import org.springframework.security.config.annotation.web.configuration.WebSecurityConfigurerAdapter;
import org.springframework.security.web.SecurityFilterChain;

@Configuration
@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {

    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http
            .authorizeRequests()
                .antMatchers("/public/**").permitAll()  // Доступ разрешен всем
                .antMatchers("/admin/**").hasRole("ADMIN")  // Только пользователям с ролью ADMIN
                .anyRequest().authenticated()  // Все остальные запросы требуют аутентификации
            .and()
            .formLogin()  // Настройка формы логина
                .loginPage("/login")
                .permitAll()
            .and()
            .logout()  // Настройка выхода из системы
                .permitAll();
    }
}
```
В этом примере:
- **authorizeRequests()**: Определяет правила авторизации для различных URL.
- **antMatchers()**: Определяет конкретные пути и применяет к ним правила доступа.
- **formLogin()**: Настраивает страницу логина.
- **logout()**: Настраивает выход из системы.

#### Современный подход с использованием `SecurityFilterChain` в Spring Security 5.4+

С введением Spring Security 5.4 и выше, появилась возможность использовать более гибкую конфигурацию, основанную на компонентах и лямбдах.

#### Пример использования `SecurityFilterChain`:
```
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.security.config.annotation.web.builders.HttpSecurity;
import org.springframework.security.core.userdetails.User;
import org.springframework.security.core.userdetails.UserDetails;
import org.springframework.security.core.userdetails.UserDetailsService;
import org.springframework.security.provisioning.InMemoryUserDetailsManager;
import org.springframework.security.web.SecurityFilterChain;

@Configuration
public class SecurityConfig {

    @Bean
    public SecurityFilterChain securityFilterChain(HttpSecurity http) throws Exception {
        http
            .authorizeRequests(authorize -> authorize
                .antMatchers("/public/**").permitAll()
                .antMatchers("/admin/**").hasRole("ADMIN")
                .anyRequest().authenticated()
            )
            .formLogin(form -> form
                .loginPage("/login")
                .permitAll()
            )
            .logout(logout -> logout
                .permitAll()
            );

        return http.build();
    }

    @Bean
    public UserDetailsService userDetailsService() {
        UserDetails user = User.withDefaultPasswordEncoder()
            .username("user")
            .password("password")
            .roles("USER")
            .build();
        
        UserDetails admin = User.withDefaultPasswordEncoder()
            .username("admin")
            .password("admin")
            .roles("ADMIN")
            .build();

        return new InMemoryUserDetailsManager(user, admin);
    }
}
```
#### Как работает `SecurityFilterChain`
1. **Запуск фильтров**: Когда HTTP-запрос поступает в приложение, он проходит через цепочку фильтров, определенных в `SecurityFilterChain`.
2. **Применение правил**: Каждый фильтр в цепочке выполняет свою задачу (например, проверка аутентификации, авторизация, обработка исключений и т.д.).
3. **Контроль доступа**: Фильтры анализируют запрос и определяют, разрешено ли ему продолжить обработку или нужно выполнить какие-то действия (например, перенаправить на страницу логина).
4. **Финальная обработка**: После прохождения всех фильтров запрос передается в конечную точку (контроллер, сервис и т.д.) для обработки бизнес-логики.
#### Пример конфигурации безопасности:
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

#### Аннотация `@PreAuthorize`
Аннотация `@PreAuthorize` — это мощный инструмент в Spring Security, который позволяет вам задавать правила авторизации на уровне методов. Она используется для определения условий, которые должны быть выполнены перед вызовом метода, что обеспечивает контроль доступа к методам на основе ролей, прав доступа и других условий безопасности.

##### Основные аспекты `@PreAuthorize`
1. **Выражения SpEL**: Аннотация использует Spring Expression Language (SpEL) для определения условий безопасности. Это позволяет гибко задавать правила авторизации.
2. **Места использования**: `@PreAuthorize` можно использовать как на уровне интерфейсов, так и на уровне реализаций методов в классах.
3. **Контроль доступа**: Аннотация проверяет условия до выполнения метода, обеспечивая предварительный контроль доступа.

##### Пример использования `@PreAuthorize`
```
import org.springframework.context.annotation.Configuration;
import org.springframework.security.config.annotation.method.configuration.EnableGlobalMethodSecurity;
import org.springframework.security.config.annotation.web.builders.HttpSecurity;
import org.springframework.security.config.annotation.web.configuration.EnableWebSecurity;
import org.springframework.security.config.annotation.web.configuration.WebSecurityConfigurerAdapter;

@Configuration
@EnableWebSecurity
@EnableGlobalMethodSecurity(prePostEnabled = true)
public class SecurityConfig extends WebSecurityConfigurerAdapter {

    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http
            .authorizeRequests()
                .anyRequest().authenticated()
            .and()
            .formLogin()
                .permitAll()
            .and()
            .logout()
                .permitAll();
    }
}
```
##### Пример сервиса с `@PreAuthorize`
```
import org.springframework.security.access.prepost.PreAuthorize;
import org.springframework.stereotype.Service;

@Service
public class MyService {

    @PreAuthorize("hasRole('ROLE_ADMIN')")
    public void adminMethod() {
        // Только пользователи с ролью ADMIN могут вызвать этот метод
        System.out.println("Admin method called");
    }

    @PreAuthorize("#id == authentication.principal.id")
    public void userMethod(Long id) {
        // Только пользователь с идентификатором, совпадающим с его собственным, может вызвать этот метод
        System.out.println("User method called");
    }

    @PreAuthorize("hasAuthority('READ_PRIVILEGE')")
    public void privilegedMethod() {
        // Только пользователи с правом доступа 'READ_PRIVILEGE' могут вызвать этот метод
        System.out.println("Privileged method called");
    }
}
```
##### Как работают выражения SpEL в `@PreAuthorize`
- **`hasRole('ROLE_NAME')`**: Проверяет, имеет ли текущий пользователь указанную роль. Роль должна быть указана с префиксом `ROLE_`.
- **`hasAuthority('AUTHORITY')`**: Проверяет, имеет ли текущий пользователь указанное право (authority).
- **`#id == authentication.principal.id`**: Сравнивает значение параметра метода с атрибутом текущего аутентифицированного пользователя. Здесь `#id` — это параметр метода, а `authentication.principal` представляет текущего аутентифицированного пользователя.
- **`@someBean.someMethod(#id)`**: Вызывает метод бина Spring с использованием SpEL. Это позволяет использовать дополнительные компоненты Spring в выражениях.

##### Пример сложного условия
Вы можете комбинировать различные условия для создания сложных правил авторизации.
```
@PreAuthorize("hasRole('ROLE_ADMIN') or (hasRole('ROLE_USER') and #id == authentication.principal.id)")
public void complexMethod(Long id) {
    // Доступ разрешен пользователям с ролью ADMIN или пользователям с ролью USER, если их идентификатор совпадает с параметром id
    System.out.println("Complex method called");
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

Mock объекты (или просто "моки") — это тестовые двойники, используемые для замены реальных объектов в тестах. Они позволяют изолировать код, который вы хотите протестировать, от его зависимостей, что делает тестирование более предсказуемым и контролируемым. Моки используются для имитации поведения реальных объектов, таких как базы данных, веб-сервисы и другие компоненты, взаимодействие с которыми может быть трудно контролировать или воспроизводить в тестах.
#### Основные концепции моков
1. **Изоляция**: Моки позволяют изолировать тестируемый код от внешних зависимостей, чтобы тесты были независимыми и предсказуемыми.
2. **Поведение и верификация**: Моки могут быть настроены для возвращения определённых значений при вызове их методов (поведение), а также для проверки того, что определённые методы были вызваны с ожидаемыми аргументами (верификация).
3. **Легковесность**: Моки создаются и уничтожаются быстро, что делает тесты более эффективными.

##### Создание и настройка моков
```
import org.junit.jupiter.api.Test;
import org.mockito.Mockito;
import static org.mockito.Mockito.*;

class UserServiceTest {

    @Test
    void testGetUserById() {
        // Создание мока
        UserRepository userRepository = mock(UserRepository.class);

        // Настройка поведения мока
        User mockUser = new User(1L, "John Doe");
        when(userRepository.findById(1L)).thenReturn(Optional.of(mockUser));

        // Создание объекта, который мы будем тестировать, с использованием мока
        UserService userService = new UserService(userRepository);

        // Вызов метода и проверка результата
        User user = userService.getUserById(1L);
        assertEquals("John Doe", user.getName());

        // Проверка, что метод был вызван с ожидаемыми аргументами
        verify(userRepository).findById(1L);
    }
}
```
#### Поведение и верификация
##### Настройка поведения
Вы можете настроить моки, чтобы они возвращали определённые значения или выбрасывали исключения при вызове методов.
```
when(mockObject.method()).thenReturn(value);
when(mockObject.method()).thenThrow(new RuntimeException());
```
##### Проверка вызовов
Mockito позволяет проверить, что методы моков были вызваны с ожидаемыми аргументами.
```
verify(mockObject).method(expectedArgument);
verify(mockObject, times(1)).method(expectedArgument);
```
### 4. Внедрение моков: использование аннотаций `@Mock`, `@InjectMocks`

Аннотация `@InjectMocks` в Mockito используется для автоматического создания экземпляра класса и внедрения в него моков. Это упрощает настройку тестов, так как позволяет автоматически подставлять моки в зависимости, что экономит время и уменьшает вероятность ошибок при ручной настройке тестов.

#### Основные аспекты работы `@InjectMocks`
1. **Автоматическое создание объекта**: Mockito создает экземпляр класса, аннотированного `@InjectMocks`.
2. **Автоматическое внедрение зависимостей**: Mockito ищет поля в этом классе и пытается автоматически внедрить моки, аннотированные `@Mock`, `@Spy` или другие.

#### Пример использования `@InjectMocks`
Рассмотрим пример, где у нас есть сервис `UserService`, который зависит от репозитория `UserRepository`.
#### Классы для тестирования
##### UserRepository
```
public interface UserRepository {
    User findById(Long id);
}
```
##### UserService
```
public class UserService {
    private UserRepository userRepository;

    public UserService(UserRepository userRepository) {
        this.userRepository = userRepository;
    }

    public User getUserById(Long id) {
        return userRepository.findById(id);
    }
}
```
Тестирование с использованием `@InjectMocks`
```
import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;
import org.mockito.InjectMocks;
import org.mockito.Mock;
import org.mockito.MockitoAnnotations;

import static org.junit.jupiter.api.Assertions.assertEquals;
import static org.mockito.Mockito.*;

public class UserServiceTest {

    @Mock
    private UserRepository userRepository;

    @InjectMocks
    private UserService userService;

    @BeforeEach
    void setUp() {
        MockitoAnnotations.openMocks(this);
    }

    @Test
    void testGetUserById() {
        User mockUser = new User(1L, "John Doe");
        when(userRepository.findById(1L)).thenReturn(mockUser);

        User user = userService.getUserById(1L);
        assertEquals("John Doe", user.getName());

        verify(userRepository).findById(1L);
    }
}
```
#### Пошаговое объяснение
1. **Аннотация `@Mock`**: Аннотирует поле `userRepository`, указывая Mockito создать мок для этого интерфейса.
2. **Аннотация `@InjectMocks`**: Аннотирует поле `userService`, указывая Mockito создать экземпляр этого класса и автоматически внедрить в него моки.
3. **Инициализация моков**: В методе `setUp()` используется `MockitoAnnotations.openMocks(this)`, чтобы инициализировать моки и внедрить их в `userService`.
4. **Настройка поведения мока**: В методе `testGetUserById()` настраивается поведение мока `userRepository`, чтобы при вызове `findById(1L)` возвращался объект `mockUser`.
5. **Вызов тестируемого метода**: Вызов метода `getUserById` на `userService` возвращает `mockUser`, и результат проверяется с помощью `assertEquals`.
6. **Проверка вызова мока**: Проверяется, что метод `findById` был вызван с аргументом `1L`.

#### Дополнительные возможности `@InjectMocks`
- **Конструктор**: Mockito может использовать конструктор для внедрения зависимостей, если конструктор присутствует.
- **Сеттеры**: Если у класса есть сеттеры, Mockito может использовать их для внедрения зависимостей.
- **Поля**: Mockito может напрямую внедрять моки в поля класса, если они доступны (не private).
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