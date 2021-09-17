# Keycloak BCrypt

Add a password hash provider to handle BCrypt passwords inside Keycloak.

## Build
```bash
./gradlew jar
```

## Test with docker-compose
```bash
cp build/libs/keycloak-bcrypt-1.6.2.jar docker/
docker-compose up -d
```

## Install
```
curl -L https://github.com/ommsolutions/keycloak-bcrypt/releases/download/1.6.2/keycloak-bcrypt-1.6.2.jar > KEYCLOAK_HOME/standalone/deployments/keycloak-bcrypt-1.6.2.jar
```
You need to restart Keycloak.

## How to use
Go to `Authentication` / `Password policy` and add hashing algorithm policy with value `bcrypt`.

To test if installation works, create new user and set its credentials.
