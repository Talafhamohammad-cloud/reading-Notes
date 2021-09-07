## What is JSON Web Token?

- JSON Web Token (JWT) is an open standard (RFC 7519) that specifies a compact and self-contained method for securely transferring information as a JSON object between two parties. Because it is digitally signed, this information can be checked and trusted. JWTs can be signed using a secret (using the HMAC technique) or with an RSA or ECDSA public/private key combination.

- Although JWTs can be encrypted to ensure party-to-party confidentiality, we'll concentrate on signed tokens. Signed tokens can be used to validate the validity of the claims they contain, whilst encrypted tokens keep such claims hidden from third parties. When public/private key pairs are used to sign tokens The signature also verifies that only the party in possession of the private key signed it.

## When should you use JSON Web Tokens?

- Here are some scenarios where JSON Web Tokens are useful:

  - Authorization: The most prevalent use case for JWT is authorization. – – Each subsequent request will contain the JWT once the user has signed in, allowing the user to access routes, services, and resources that are authorized with that token. Single Sign On is a popular feature that makes use of JWT nowadays due to its low overhead and ability to be utilized across many domains.

    -Information Exchange: JSON Web Tokens are a safe means of exchanging data between parties. You can be sure the senders are who they say they are because JWTs may be signed—for example, using public/private key pairs. You may also check that the content hasn't been changed with because the signature is computed using the header and payload.

## JSON Web Token structure

1- Header

2- Payload

3- Signature

## How do JSON Web Tokens work?

- In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned. Since tokens are credentials, great care must be taken to prevent security issues. In general, you should not keep tokens longer than required.

- You also should not store sensitive session data in browser storage due to lack of security.
- Whenever the user wants to access a protected route or resource, the user agent should send the JWT, typically in the Authorization header using the Bearer schema.
- how a JWT is obtained and used to access APIs or resources:
- The application or client requests authorization to the authorization server. This is performed through one of the different authorization flows. For example, a typical OpenID Connect compliant web application will go through the /oauth/authorize endpoint using the authorization code flow.
- When the authorization is granted, the authorization server returns an access token to the application.
- The application uses the access token to access a protected resource (like an API).

- Do note that with signed tokens, all the information contained within the token is exposed to users or other parties, even though they are unable to change it. This means you should not put secret information within the token.

## Why should we use JSON Web Tokens?

- As JSON is less verbose than XML, when it is encoded its size is also smaller, making JWT more compact than SAML. This makes JWT a good choice to be passed in HTML and HTTP environments.
- Security-wise, SWT can only be symmetrically signed by a shared secret using the HMAC algorithm. However, JWT and SAML tokens can use a public/private key pair in the form of a X.509 certificate for signing. Signing XML with XML Digital Signature without introducing obscure security holes is very difficult when compared to the simplicity of signing JSON.
- JSON parsers are common in most programming languages because they map directly to objects. Conversely, XML doesn't have a natural document-to-object mapping. This makes it easier to work with JWT than SAML assertions.
- Regarding usage, JWT is used at Internet scale. This highlights the ease of client-side processing of the JSON Web token on multiple platforms, especially mobile.