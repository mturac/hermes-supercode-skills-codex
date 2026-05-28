# OAuth2 Flow Reference

1. Use authorization code with PKCE for browser-based and mobile login.
2. Use OIDC when the application needs user identity, not just API access.
3. Validate `iss`, `aud`, `exp`, `iat`, `nonce`, and token signature.
4. Store web sessions in secure, HTTP-only cookies where possible.
5. Do not store long-lived tokens in local storage for browser apps.
6. Use client credentials only for service-to-service calls.
7. Keep client secrets out of public clients.
8. Use least-privilege scopes for every client.
9. Rotate refresh tokens and revoke the token family on replay.
10. Keep access tokens short-lived, commonly 5 to 15 minutes.
11. Use refresh tokens only with confidential clients or strong sender controls.
12. For SAML, validate signature, audience, recipient, and time conditions.
13. Prefer OIDC over SAML for new integrations when the provider supports it.
14. Use state parameters for CSRF protection in OAuth redirects.
15. Use PKCE even for confidential clients when the library supports it.
16. Never accept unsigned JWTs.
17. Use JWKS with `kid` for asymmetric key rotation.
18. Separate authentication from authorization decisions.
19. Log auth events without logging token values.
20. Test failure paths as thoroughly as successful login.
21. Document callback URLs per environment.
