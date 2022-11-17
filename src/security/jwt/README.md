# Encryption

> encoding transforms data into another format using a schema that publicly
> available so that it can easily be revered
>
>encryption transforms data into another format in such a way that only specific individual can reverse the transformation

- [`encryption techniques`](#encryption-techniques)

<br>

### encryption techniques

- symmetric encryption: private-key cryptography
- asymmetric encryption: public-key cryptography

**asymmetric encryption**

> - private key to kept secret
> - public key to be shared

**asymmetric algorithm**

> - AES
> - DES
> - RSA

**asymmetric use case**

> - SSH
> - TLS
> - Bitcoin

<br>

[↑ top](#encryption)
<br><br><br><br><hr>

# JWT

> jwt is a string made up of three parts, separated by dots, and serialized using base64
>
> header (token type, algorithm used to sign the token) <br>
> payload (iss, exp, sub, aud) <br>
> signature

- [`jwt types`](#jwt-types)
- [`jwt authentication`](#jwt-authentication)

[↑ top](#jwt)
<br><br><br><br><hr>

### jwt types

<br>

jwt has two kinds of token:

- id token used for application
- access token used for protect api

<br>

[↑ top](#jwt)
<br><br><br><br><hr>

### jwt authentication

<br>

> - OAuth 2.0 is authorization framework and uses Access Token and Refresh Token.
> - OpenID Connect(ODDC) is identity protocol to performs user authentication. OIDC uses ID Tokens

**invalidate token:**

<br>

- creating a blacklist: using redis to create blacklist token
- introduce refresh token

refresh token can be stored in local storage

**how to secure refresh token:**

- Automatic Reuse Detection
- Introduce lifetime expiration ( absolute lifetime & inactivity lifetime)

**Steps to validate access token:**

- perform standard JWT validation
- verify token audience claims
- verify permission (scopes)

<br>

[↑ top](#jwt)
<br><br><br><br><hr>
