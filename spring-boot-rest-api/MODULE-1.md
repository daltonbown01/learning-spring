# Module 1

## Spring VS Spring Boot

**Spring**

- Giant framework with lots of modules
    - e.g., _Spring MVC_ for web apps, _Spring Data_ for data access, etc.
- Requires a lot of configuration

**Spring Boot**

- Opinionated Spring (i.e., pre-configured with a popular config) => simpler
- Includes an embedded web server

## Inversion of Control Container (IoC)

- Allows control over how and when dependencies are provided to the app
- e.g., simpler mechanism to handle difference databases for local VS prod
- Often called _dependency injection (DI)_
    - Technically DI is a way to achieve IoC

## Spring Initializr

- Bootstrapper for Spring Boot

## API Contracts

- Programmatic way for consumers and APIs to agree upon API behaviour

## Test Driven Development (TDD)

- Writing test before implementation
- Enforces we write minimal code to satisfy implementation

## Testing Pyramid

- Unit tests exercise isolated units of functionality
    - Ideally the highest ratio of tests
- Integration tests exercise groups of functional units
- End-to-end (E2E) tests exercise using the same interface as end users
    - Ideally the smallest number of tests

## Red, Green, Refactor Loop

- Refactoring is easier when you have a robust suite of tests
- Cycle:
    - Red: Write failing tests to outline desired functionality
    - Green: Implement the simplest code to pass the tests
    - Refactor: Improve the code without failing the tests

## REST

- Representational State Transfer
- Resource-based
- CRUD
    - Create via HTTP POST returns 201 (CREATED)
    - Read via HTTP GET returns 200 (OK)
    - Update via HTTP PUT returns 204 (NO DATA)
    - Delete via HTTP DELETE returns 204 (NO DATA)
- HTTP = Hypertext Transfer Protocol

## REST in Spring Boot

- Configures and instantiates objects @ boot called Spring beans
- Component scan phase @ app startup
- Beans are stored in Spring's IoC container

## Spring Web Controllers

- Annotate with `@RestController` to route API requests to
- Add methods to these controllers to handle API requests
    - Annotate with `@GetMapping` to map HTTP GET requests for a specific URI
- Use `@PathVariable` for path variables
- Use `ResponseEntity` to deliver the response

## Layered Architecture

- Controller interfaces to the client invoking the API
- Need to separate concerns => controller can't retrieve the data
- Repository will handle the data, either an in-memory DB or a persistent DB
- Spring Boot uses H2 as the in-memory DB

## Spring Data's CrudRepository

- Provides predefined methods for CRUD apps