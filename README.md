# HelloSign Frontend Tester Page with ReactJS

This page was created to test HelloSign API's Embedded Requesting, Embedded Signature Requests, and Embedded Templates.

## Getting Started

**Install**

http-server: `npm -g install http-server` [More Info](https://www.npmjs.com/package/http-server)

**To start server:** `$ http-server`

You will see a list of available ports that the http-server is serving on

Example:

```
Starting up http-server, serving ./
Available on:
  http://127.0.0.1:8081
  http://10.0.9.208:8081
  http://10.0.9.211:8081
  http://169.254.204.12:8081
```

**To stop the server:** `CTRL-C`

## HelloSign API Walkthroughs

1. [Embedded Signing](https://app.hellosign.com/api/embeddedSigningWalkthrough) - [Client Side](https://app.hellosign.com/api/embeddedSigningWalkthrough#EmbeddedSigningClientSide)
2. [Embedded Requesting](https://app.hellosign.com/api/embeddedRequestingWalkthrough) - [Client Side](https://app.hellosign.com/api/embeddedRequestingWalkthrough#EmbeddedRequestingClientSide)
3. [Embedded Templates](https://app.hellosign.com/api/embeddedTemplatesWalkthrough)

## Testing use cases

1. **Embedded Signing** - Create an embedded signature request with or without a template (the template can be create on hellosign.com). You will need the `signature_id` (for each signer) to get the embedded `sign_url` (for each signer) and complete the signature request in the iFrame.
2. **Embedded Requesting** - Create an embedded uncliamed draft and use the `claim_url` to complete the request for signature in the iFrame.
3. **Embedded Templates** - Create an embedded template draft and use the `edit url` to edit the template in the iFrame. 

## More Info
This frontend tester page is complimentary to separately use with the Node.js backend found [here](https://github.com/latoyazamill/hellosign-console-app).
