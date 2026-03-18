# Application Security Research Notes
This repository contains structured observations derived from testing real-world web applications.
The focus is on identifying trust boundaries, analyzing system behavior, and documenting security-relevant patterns across authentication, session management, API design, and business logic.


## Sections

- [Session Management Analysis](./Session-Management-Analysis.md)
- [Authentication Flow Analysis](./Authentication-Flow-Analysis.md)
- [API Behavior & Access Patterns](./API-Behavior-and-Access-Patterns.md)
- [Business Logic Observations](./Business-Logic-Observation.md)

---

## Approach

Testing focuses on understanding how applications are designed to function and identifying where trust assumptions can be broken.

Rather than relying solely on automated tools, the emphasis is placed on:

- Observing real application behavior  
- Replaying and modifying requests  
- Identifying trust boundaries  
- Validating assumptions through testing
