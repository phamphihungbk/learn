# JWT

> encoding transforms data into another format using a schema that publicly
> available so that it can easily be revered
>
>encryption transforms data into another format in such a way that only specific individual can reverse the transformation

- [`encryption`](#encryption)
- [`jwt`](#jwt)

[↑ top](#jwt)
<br><br><br><br><hr>

### `encryption`

<br>

**encryption techniques**

> - symmetric encryption: private-key cryptography
> - asymmetric encryption: public-key cryptography

**asymmetric encryption techniques**

> - private key to kept secret
> - public key to be shared

**asymmetric algorithm**

> - AES
> - DES
> - RSA

**use case**

> - SSH
> - TLS
> - Bitcoin

<br>

[↑ top](#jwt)
<br><br><br><br><hr>

### `jwt`

<br>

> jwt is a string made up of three parts, separated by dots, and serialized using base64
>
> header (token type, algorithm used to sign the token) <br>
> payload (iss, exp, sub, aud) <br>
> signature

jwt has two kinds of token:

- id token used for application
- access token used for protect authorization

<br>

[↑ top](#jwt)
<br><br><br><br><hr>
