# Authorization Header

> <- Back to [[HTTP Headers]]

Carries credentials for authenticating the client. Common schemes: Bearer (token-based, used with OAuth/JWT), Basic (base64-encoded username:password, must use HTTPS), and API key. The server responds with 401 and WWW-Authenticate header when authentication is required.

#networking #http #security
