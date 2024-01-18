# ADR-002: Autonomous Bubble Context For Integration with Legacy Accounting System

### Status

Accepted, Supersedes [ADR001](adr-001-bubble-context-for-integration-with-legacy-accounting-system.md)

### Context

Having the bubble context direct dependency on the database of legacy system, we are somehow highly coupled to the failures of that system.........

### Decision

Transforming the current bubble context into an Autonomous Bubble context which stores the needed data in itself and sync with the legacy system periodically. with this solution, ..........
