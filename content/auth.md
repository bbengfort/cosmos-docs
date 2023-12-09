---
weight: 11
title: Authentication
---

# Authentication

> The claims in an access token are structured as follows:

```json
{
  "iss": "https://api.cosmosgame.space",
  "sub": "1",
  "aud": [
    "https://cosmosgame.space"
  ],
  "exp": 1702224504,
  "nbf": 1702138104,
  "iat": 1702138104,
  "jti": "01HH7NCJVRHAVRQVNWMZJFCHMZ",
  "name": "Benjamin Bengfort",
  "email": "benjamin@bengfort.com",
  "role": "Admin",
  "permissions": [
    "users:manage",
    "games:read",
    "games:create",
    "games:manage"
  ]
}
```

Most API calls must be authenticated using a [JWT](https://jwt.io) access token provided as a `Bearer` token in the `Authorization` header (alternatively the access token can be specified using secure cookies set by the server). Access tokens expire after 24 hours but can be refreshed using a refresh token. Both the access token and refresh token are created for a user after logging in.

The access token embeds claims that you can parse and use in your application if you'd like, for example to display a gravatar based on the user's email address or to store information about players using their user ID. These claims also influence API behavior not just for authentication and authorization but also to return only that player's specific information.

