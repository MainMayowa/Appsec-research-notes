### Persistent Session After Logout

During testing, it was observed that logging out of the application does not invalidate previously issued authentication tokens.

After logout:
- The token is removed on the client side
- However, the same token remains valid when reused in subsequent requests

This was confirmed by manually sending authenticated requests using a previously issued token after logout, which continued to return authorized responses.

Additionally:
- Multiple tokens can remain valid simultaneously for the same account
- Logging in again generates a new token without invalidating older ones

Impact:
If a token is exposed (e.g., via interception or leakage), an attacker can maintain access even after the user logs out.

Observation:
Session invalidation appears to be handled only on the frontend, with no server-side revocation mechanism.
