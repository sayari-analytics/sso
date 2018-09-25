# Run
```bash
cd quickstart/
docker-compose up -d
```

Upstream services are defined in `./quickstart/upstream_configs.yml`.  Containers are definined in `./quickstart/docker-compose.yml`.x

# NIFI Instructions
- sign in: `http://nifi.sso.localtest.me/nifi/`
- if unauthenticated, sign in w/ `@sayari.com` or `@sayarianalytics.com` account
- sign out via `http://nifi.sso.localtest.me/oauth2/sign_out`
- errors
  - 409 conflict errors from
    - `POST http://nifi.sso.localtest.me/nifi-api/access/kerberos 409`
    - `POST http://nifi.sso.localtest.me/nifi-api/access/oidc/exchange 409`
    - `GET http://nifi.sso.localtest.me/nifi-api/flow/controller/bulletins 500`
    - `GET http://nifi.sso.localtest.me/nifi-api/flow/status 500`

# Schema Registry Instructions
- sign in: `http://schema-registry.sso.localtest.me`
- if unauthenticated, sign in w/ `@sayari.com` or `@sayarianalytics.com` account
- sign out via `http://schema-registry.sso.localtest.me//oauth2/sign_out`

# Development
- after editing either `docker-compose.yml` or `upstream_configs.yml`, run `docker-compose restart`

# Notes
- access nifi at `http://nifi.sso.localtest.me/nifi/`, not `http://nifi.sso.localtest.me`.  The nifi root url will redirect `http://nifi.sayari.com:9090/nifi`, bypassing the proxy
