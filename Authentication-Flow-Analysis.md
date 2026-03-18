### OTP Request and Validation Behavior

The application uses an OTP-based authentication mechanism for user login.

During testing, the OTP flow was analyzed by observing the requests sent to the authentication endpoint and modifying inputs where possible.

Observations:

- OTP requests can be triggered repeatedly without any visible rate limiting
- The system returns the same response for both valid and invalid login attempts, providing no clear distinction between existing and non-existing users
- OTP validity differs depending on user type (e.g., standard users vs admin/Omni users)

Further testing showed that:

- Repeated OTP requests within a short timeframe did not appear to be restricted
- OTP reuse was not allowed, indicating some level of validation on the backend
- However, lack of request throttling increases the potential for abuse

Impact:

The absence of rate limiting on OTP requests may allow an attacker to abuse the authentication system through repeated requests, potentially leading to denial-of-service conditions or targeted abuse of specific user accounts.

Additionally, inconsistent OTP handling across user roles may introduce unintended differences in security posture between account types.

Observation:

While OTP validation exists, protections around OTP request generation appear insufficient.
