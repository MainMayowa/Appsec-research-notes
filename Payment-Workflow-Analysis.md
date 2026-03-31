## Payment Workflow Analysis (Food Ordering Platform)

### Context
Tested a live food ordering platform focusing on the checkout and payment process.

### Flow Tested
Cart → Checkout → Payment

### What I Observed
The application accepts client-controlled input during the payment process before backend validation.

### What I Did
Intercepted the request during payment and modified relevant parameters to observe how the backend processes transaction values.

### Impact
Transaction integrity could be affected if client-controlled values are trusted, potentially allowing incorrect payment amounts or manipulation of transaction behavior.

### Why It Happens
The backend appears to rely on values provided by the client instead of strictly validating them server-side.

### Recommended Fix
Enforce server-side validation for all transaction-related values and ensure payment amounts are derived and verified on the backend before processing.
