# Run
```bash
docker-compose up -d
```

# NIFI instructions
- to sign in: `http://nifi.sso.localtest.me/nifi/`
- if unauthenticated, sign in w/ `@sayari.com` or `@sayarianalytics.com` account
- sign out via `http://nifi.sso.localtest.me/oauth2/sign_out`
- errors
  - 409 conflict errors from
    - `POST http://nifi.sso.localtest.me/nifi-api/access/kerberos 409`
    - `POST http://nifi.sso.localtest.me/nifi-api/access/oidc/exchange 409`
    - `GET http://nifi.sso.localtest.me/nifi-api/flow/controller/bulletins 500`
    - `GET http://nifi.sso.localtest.me/nifi-api/flow/status 500`
