<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@stripe/firestore-stripe-payments](./firestore-stripe-payments.md) &gt; [createCheckoutSession](./firestore-stripe-payments.createcheckoutsession.md)

## createCheckoutSession() function

Creates a new Stripe checkout session with the given parameters. Returned session contains a session ID and a session URL that can be used to redirect the user to complete the checkout. User must be currently signed in with Firebase Auth to call this API. If a timeout occurs while waiting for the session to be created and acknowledged by Stripe, rejects with a `deadline-exceeded` error. Default timeout duration is [CREATE\_SESSION\_TIMEOUT\_MILLIS](./firestore-stripe-payments.create_session_timeout_millis.md)<!-- -->.

<b>Signature:</b>

```typescript
export declare function createCheckoutSession(payments: StripePayments, params: SessionCreateParams, options?: CreateCheckoutSessionOptions): Promise<Session>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  payments | [StripePayments](./firestore-stripe-payments.stripepayments.md) | A valid [StripePayments](./firestore-stripe-payments.stripepayments.md) object. |
|  params | [SessionCreateParams](./firestore-stripe-payments.sessioncreateparams.md) | Parameters of the checkout session. |
|  options | [CreateCheckoutSessionOptions](./firestore-stripe-payments.createcheckoutsessionoptions.md) | Optional settings to customize the behavior. |

<b>Returns:</b>

Promise&lt;[Session](./firestore-stripe-payments.session.md)<!-- -->&gt;

Resolves with the created Stripe Session object.

