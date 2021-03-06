# Crypt service documentation

## Index

* [Description](#Description)
* [Methods](#Methods)
  * [generateJWT](#generateJWT)
  * [verifyJWT](#verifyJWT)
  * [hash](#hash)

## Description

This service is in charge of perform cryptographic processes.

## Methods

### `generateJWT`

* **Description**: Generates a JSON web token using the RSA SHA256 algorithm implementation provided by the `sign` method 
of the [jsonwebtoken library](https://www.npmjs.com/package/jsonwebtoken). It returns the JWT.
* **Params**: 
  * `payload`: Object
  * `expiresIn`: int | string
* **Return data type**: Promise\<string>

### `verifyJWT`

* **Description**: Verifies the signature of a JWT generated by `generateJWT` method of this service. 
If the token is valid, returns the decoded payload.
* **Params**: 
  * `token`: string
* **Return data type**: Promise\<Object>

### `hash`

* **Description**: Hash an string using the SHA256 algorithm.
* **Params**: 
  * `data`: string
* **Return data type**: string
