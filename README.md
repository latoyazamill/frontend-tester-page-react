# HelloSign Frontend Tester Page with ReactJS

This page was created to test HelloSign API's Embedded Requesting, Embedded Signature Requests, and Embedded Templates.

Deployed app - [Here](https://frontend-tester-page-react.herokuapp.com)

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

1. Embedded Signing - [Client Side](https://app.hellosign.com/api/embeddedSigningWalkthrough#EmbeddedSigningClientSide)
2. Embedded Requesting - [Client Side](https://app.hellosign.com/api/embeddedRequestingWalkthrough#EmbeddedRequestingClientSide)
3. [Embedded Templates](https://app.hellosign.com/api/embeddedTemplatesWalkthrough)

## Testing use cases

You will need your Client Id for each of the test cases below. Your Client Id can be found by logging in to [hellosign.com](https://app.hellosign.com/home/myAccount#api), navigating to your settings, clicking on API in the top navigation bar, and looking within the "API App" section on that page.

After you get your Client Id, you will need to complete one of the following request to retrieve the `sign_url`, `claim_url`, or `edit_url`.

1. **Embedded Signing** - 
- Create an [embedded signature request](https://app.hellosign.com/api/embeddedSigningWalkthrough) with or without a template (the template can be create on hellosign.com). 
- You will need the `signature_id` (for each signer) to get the embedded `sign_url` (for each signer) and complete the signature request in the iFrame.
2. **Embedded Requesting** - 
- Create an [embedded uncliamed draft](https://app.hellosign.com/api/embeddedRequestingWalkthrough) and use the `claim_url` to complete the request for signature in the iFrame.
3. **Embedded Templates** - 
- Create an embedded template draft and use the `edit url` to edit the template in the iFrame. 

If the above request was create in `test_mode` then you skip the domain verification by checking the box next to `Skip domain verification?`. 

**Potential bug** when using `Close and redirect?`

You will receive and error message of *"'X-Frame-Options' to 'sameorigin'"* if the tests (parent page) are **not** being done from the same domain as your site page, the site page cannot be included in the iFrame. [More Info](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options)

## More Info
This frontend tester page is complimentary to separately use with the Node.js backend found [here](https://github.com/latoyazamill/hellosign-console-app).
