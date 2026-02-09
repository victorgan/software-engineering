# CORS Preflight

> <- Back to [[HTTP Methods]]

Before sending certain cross-origin requests (non-simple methods, custom headers), browsers send an OPTIONS preflight request to check if the server allows it. The server responds with Access-Control-Allow-* headers. Preflight results are cached to avoid repeated checks (Access-Control-Max-Age).

#networking #http #security
