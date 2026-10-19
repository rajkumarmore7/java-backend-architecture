
# ADR-001: Java and Spring Boot Technology Baseline

- Status: Accepted
- Date: 2026-10-18
- Project: java-backend-architecture
- Decision Owner: Rajkumar Vijay More

## Context

The Java Backend Architecture project is a
public engineering portfolio demonstrating modern
backend development and microservices architecture.

The project needs a stable, maintainable technology
baseline suitable for progressive development.

## Decision

The following technology versions are selected:

| Component | Decision |
|---|---|
| Java | Java 21 LTS |
| Spring Boot | 4.1.1 |
| Spring Framework | 7.x (managed by Boot) |
| Build Tool | Apache Maven |
| Java Packaging | Executable JAR |

The project will use Java 21 language features,
including records, pattern matching, and virtual
threads where they provide measurable benefits.

Spring Boot dependency management will control
compatible Spring ecosystem dependencies.

## Rationale

### Java 21 LTS

- Long-term support release
- Mature enterprise ecosystem
- Records and modern language features
- Virtual threads available for suitable workloads
- Strong compatibility with modern Spring Boot

### Spring Boot 4.1.1

- Stable Spring Boot 4 release
- Supports Java 21
- Uses Spring Framework 7
- Supports modern Jakarta APIs
- Provides production-oriented capabilities

## Consequences

### Positive

- Modern Java and Spring ecosystem
- Consistent dependency management
- Suitable foundation for backend portfolio work
- Opportunity to demonstrate current practices

### Trade-offs

- Spring Boot 4 adopts Jakarta EE 11 APIs
- Third-party compatibility must be verified
- Older examples and dependencies may need updates
- Team members require a Java 21 development environment

## Implementation Guidelines

- Configure Java 21 in Maven
- Use Spring Boot parent dependency management
- Pin the Spring Boot version
- Use Maven Wrapper for reproducible builds
- Include automated compilation and testing
- Avoid unnecessary dependency version overrides

## Validation Criteria

- Java 21 installed and verified
- Maven build succeeds
- Spring Boot application starts successfully
- Unit tests execute successfully
- Dependency compatibility verified

## Related Decisions

- ADR-002: Repository and Maven Module Structure
- ADR-003: Authentication and Security Architecture
- ADR-004: Database Ownership and Isolation
