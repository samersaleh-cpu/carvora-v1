# CARVORA International Payments

## Requirement
CARVORA Pro must be purchasable by customers outside Palestine. The payment system must accept international cards and support recurring monthly subscriptions.

## Current provider target
**Primary candidate: NeoCash**

Its published Palestinian e-commerce gateway advertises:
- recurring payments
- card tokenization
- multiple currencies
- payment from cards worldwide
- website/app integration

**Fallback candidate: Bank of Palestine Online Payment Gateway**

Its published gateway advertises:
- Visa and Mastercard acceptance locally and internationally
- multiple currencies
- website integration

## Security architecture
1. User selects Pro at $5/month.
2. CARVORA server creates or redirects to the provider checkout.
3. Provider handles card data; CARVORA never stores raw card numbers.
4. Provider sends a signed server-to-server payment/subscription event.
5. Backend verifies the event and updates the user's Pro entitlement.
6. Frontend reads the verified entitlement from the backend.
7. Cancellation, failed renewal, refund, and expiry events revoke or change the entitlement.

## Not implemented yet
The repository is currently a static GitHub Pages application. Live billing cannot be safely activated until the merchant account, provider credentials, checkout/API documentation, webhook support, and a small server-side entitlement service are available.

Never put merchant secrets, API keys, webhook signing secrets, or payment credentials into the public repository.
