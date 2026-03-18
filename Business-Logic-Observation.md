### Workflow and Trust Assumptions

During testing, attention was given to how the application expects normal user actions to occur and whether those assumptions could be manipulated.

Rather than focusing on individual endpoints, the testing approach involved interacting with the application as a normal user while observing how data flows between the frontend and backend.

Key observations included:

- Application behavior is heavily dependent on client-initiated requests
- Certain actions rely on values sent from the client rather than independently derived on the server
- Workflow execution (such as login, session usage, and API interaction) assumes that requests follow an expected sequence

Testing approach:

- Observe how the application behaves during normal usage
- Replay and modify requests where possible
- Identify where trust is placed on client-controlled data or expected flow

Security relevance:

Business logic vulnerabilities often arise not from technical flaws, but from incorrect assumptions about how users will interact with the system.

Observation:

Understanding the intended workflow of an application provides insight into where trust boundaries may be incorrectly enforced or bypassed.
