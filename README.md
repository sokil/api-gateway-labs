# api-gateway-labs

API Gateways research

## Lab setup

Add to your `/etc/hosts`:

```
127.0.0.1 keycloak
```

### Keycloak

1. Create realm `Application`
2. Create client 
   1. Create client with id `krakend` and `Access type`: `confidential`
   2. Enable `Service Accounts Enabled`. This enables Oauth2 Client Credentials grant
   3. On `Credentials` tab choose `Client Authenticator`: `Client id and secret`
   4. Create roles `time_reader` and `weather_reader`
3. Create user 
   1. Create user with name `user_with_permissions` with password `user_with_permissions`
   2. Add roles `time_reader` and `weather_reader` to it.
