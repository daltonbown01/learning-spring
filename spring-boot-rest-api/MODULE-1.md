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