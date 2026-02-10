# Token Rotation

> <- Back to [[Refresh Tokens]]

The practice of issuing a new refresh token each time one is used, invalidating the old one. Token rotation detects token theft: if a stolen token is used after the legitimate client has already rotated it, the authorization server can revoke the entire token family.

#authentication #oauth #token-rotation
