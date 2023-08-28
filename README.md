# Flutter Clean Architecture TDD (Reso Coder Style)

### About

Find more details about the Flutter Clean Architecture TDD from [Reso Coder](https://resocoder.com/flutter-clean-architecture-tdd).

# Explanation & Project Organization

Welcome to the Flutter Clean Architecture and Test-Driven Development (TDD) documentation. This guide will help you understand the principles of Clean Architecture and how to implement it using Flutter while following the TDD approach.


## Introduction

Clean Architecture is a software design philosophy that emphasizes separation of concerns and maintainability. Test-Driven Development (TDD) is a development process where tests are written before the actual code, ensuring better code quality and test coverage.

## Clean Architecture

Clean Architecture consists of different layers, each with its own responsibility:

- **Presentation Layer**: Handles UI components, widgets, and user interactions.
- **Domain Layer**: Contains the business logic and use cases of the application.
- **Data Layer**: Manages data sources, repositories, and external services.

## Implementation Steps

### Setting Up Your Project

1. Create a new Flutter project using `flutter create`.
2. Add necessary packages.
```sh
flutter pub add http ui_tool get_it flutter_bloc equatable dartz shared_preferences
```

3. Add necessary dependencies for testing, such as `test` and `mockito`.
   

### Creating Layers

1. Set up the project structure with separate folders for each layer (presentation, domain, data).
2. Define the core business logic and entities in the domain layer.
3. Implement use cases that interact with the domain layer.

#### Presentation Layer:
This layer deals with the user interface (UI), user interactions, and how data is displayed to the user. It includes widgets, screens, and components that users interact with. The primary goal of this layer is to present data to the user and receive user input.

* Create folders like **screens**, **widgets**, or **pages** to organize your UI components.
* Keep UI logic minimal and delegate most of the business logic to the domain layer.
* Use frameworks like **BLoC**, **Provider**, or **Riverpod** for state management.


#### Domain Layer:
The domain layer contains the core **business logic**, **entities**, and **use cases** of your application. It represents the heart of your application and is independent of any external framework or technology.

* Define the core business entities that represent the core concepts of your application.
* Implement use cases that encapsulate specific interactions or operations in your application.
* This layer should not depend on any external libraries or UI concerns.

#### Data Layer:
The data layer handles **data sources**, **repositories**, and **external services**. It's responsible for fetching and managing data from various sources, such as databases, APIs, or local storage.

* Implement data sources like APIs, databases, and local storage.
* Create repositories that act as an abstraction over data sources and provide a unified API for the domain layer to access data.
* Use dependency injection to provide data sources and repositories to other layers.

## Test-Driven Development (TDD)

TDD follows a cycle: Red-Green-Refactor.

1. **Red**: Write a failing test for the new feature.
2. **Green**: Write the minimal code required to make the test pass.
3. **Refactor**: Refactor the code while ensuring the test still passes.