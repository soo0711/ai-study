# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Purpose

This is a **learning repository** for experimenting with Claude Code features (skills, commands, hooks, agents). The Spring Boot application is a minimal scaffold—the focus is on observing Claude's behavior with different rules and patterns, not on building production functionality.

## Build Commands

Windows 환경에서는 `.\gradlew`, Unix/Mac에서는 `./gradlew` 사용.

```bash
.\gradlew build          # 빌드
.\gradlew bootRun        # 실행
.\gradlew test           # 전체 테스트
.\gradlew clean build    # 클린 빌드

# 단일 테스트 실행
.\gradlew test --tests "com.ai_study.AiStudyApplicationTests"
.\gradlew test --tests "com.ai_study.AiStudyApplicationTests.contextLoads"
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
  → Acts like a Facade: coordinates multiple domain and service calls
  for a single use case scenario, hiding internal complexity from the controller.
- service: supporting domain logic
- domain: core business models and rules
- repository: data access abstraction

## Rules

- Do not assume production-level requirements
- Prefer explaining design intent over generating large amounts of code
- Do not create files unless explicitly asked to implement

## Notes

- Package name uses underscore (`com.ai_study`) because `com.ai-study` is invalid in Java
- This repo prioritizes experimenting with Claude Code configuration over working application code

