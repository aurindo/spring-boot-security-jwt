# spring-boot-security-jwt
 Spring Boot application that makes use of JWT authentication for securing an exposed REST API


1. Generate JSon Web Token
```agsl
curl --location 'localhost:8080/authenticate' \
--header 'Content-Type: application/json' \
--data '{
    "username":"javainuse",
    "password":"password"
}'
```

2. Validate JSon Web Token
NOTE: Use the JWT generated on the previous request.
```agsl
curl --location 'localhost:8080/hello' \
--header 'Authorization: Bearer <JSon Web Token>'
```
