# Secure and HttpOnly Flags

> <- Back to [[Cookies and Sessions]]

Secure flag ensures the cookie is only sent over HTTPS, preventing interception on unencrypted connections. HttpOnly flag prevents JavaScript from accessing the cookie via document.cookie, mitigating XSS-based cookie theft. Both should always be set on session cookies.

#networking #http #security
