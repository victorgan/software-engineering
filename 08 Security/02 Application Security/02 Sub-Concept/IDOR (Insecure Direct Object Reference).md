# IDOR (Insecure Direct Object Reference)

> <- Back to [[Broken Access Control]]

A vulnerability where an application exposes internal object references (IDs) and fails to verify that the requesting user has authorization to access the referenced object. Example: changing /api/users/123 to /api/users/456 to access another user's data.

#application-security #access-control #idor
