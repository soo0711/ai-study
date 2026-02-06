# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Purpose

This is a **learning repository** for experimenting with Claude Code features (skills, commands, hooks, agents). The Spring Boot application is a minimal scaffold—the focus is on observing Claude's behavior with different rules and patterns, not on building production functionality.

## Build Commands

```bash
# Build the project
./gradlew build

# Run the application
./gradlew bootRun

# Run all tests
./gradlew test

# Run a single test class
./gradlew test --tests "com.ai_study.AiStudyApplicationTests"

# Run a single test method
./gradlew test --tests "com.ai_study.AiStudyApplicationTests.contextLoads"

# Clean build
./gradlew clean build
```

## Tech Stack

- Java 17
- Spring Boot 4.0.2
- Gradle (Groovy DSL)
- JUnit 5 (Jupiter) for testing

## Directory Layout

```
src/main/java/com/ai_study/    # Application code
src/test/java/com/ai_study/    # Test code
```

Main entry point: `AiStudyApplication.java`

## Project Structure (Conceptual Layers)

- controller: HTTP request/response only
- usecase: application-level orchestration
- service: supporting domain logic
- domain: core business models and rules
- repository: data access abstraction

## Rules

- Do not assume production-level requirements
- Prefer explaining design intent over generating large amounts of code

## Notes

- Package name uses underscore (`com.ai_study`) because `com.ai-study` is invalid in Java
- This repo prioritizes experimenting with Claude Code configuration over working application code

