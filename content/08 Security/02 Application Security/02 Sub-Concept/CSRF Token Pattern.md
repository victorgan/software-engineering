# CSRF Token Pattern

> <- Back to [[Cross-Site Request Forgery (CSRF)]]

A server-generated, unpredictable token included in forms and validated on submission. Since the attacker cannot read the token from the target domain (same-origin policy), they cannot include it in forged requests. CSRF tokens are typically stored in the session and included as hidden form fields.

#application-security #csrf #tokens
