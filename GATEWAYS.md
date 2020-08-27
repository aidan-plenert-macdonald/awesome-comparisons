# Gateways

Typically called API Gateways, but it's overloaded a bit.

**Disclosure**: I have a lot more experience with API Gateway. If I don't add a link to the "no" answer, then it's implicit based on me not finding an answer.

## Brief Feature Comparision

|  Feature | [AWS API Gateway](https://aws.amazon.com/api-gateway/) | [Tyk](https://tyk.io/api-gateway/open-source/) | [Kong](https://konghq.com/kong/) | [Express Gateway](https://www.express-gateway.io/) |
| --- | --- | --- | --- | --- |
| Open Source? | No | Yes | Yes | Yes |
| Free? | No | Yes | Yes | Yes |
| Can deploy locally? | [Community Docker, I had problems](https://stackoverflow.com/questions/44547574/create-api-gateway-in-localstack/48682628) | [Docker](https://tyk.io/docs/getting-started/installation/with-tyk-on-premises/docker/) | [Docker](https://docs.konghq.com/install/docker/) | [Docker](https://hub.docker.com/_/express-gateway) |
| Import Swagger? | [Web UI](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-create-api-from-example.html), [CLI](https://docs.aws.amazon.com/cli/latest/reference/apigateway/import-rest-api.html) | [Yes](https://tyk.io/docs/tyk-configuration-reference/import-apis/) | [Maybe plugin](https://docs.konghq.com/hub/optum/kong-spec-expose/) | [Don't think so](https://www.express-gateway.io/eg-vs-amazon-aws-api-gateway/) |
| Export Swagger? | [Yes](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-export-api.html) | No | No | No |
| [Swagger Extensions?](https://swagger.io/docs/specification/2-0/swagger-extensions/) | [Yes](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-swagger-extensions.html) | No | No | No |
| **Integrations** |
| AWS Lambda Integration? | [Yes](https://docs.aws.amazon.com/apigateway/latest/developerguide/getting-started-with-lambda-integration.html) | [No](https://github.com/TykTechnologies/tyk/issues/124) | [Plugin](https://docs.konghq.com/hub/kong-inc/aws-lambda/) | [Yes](https://www.express-gateway.io/docs/policies/lambda/) |
| HTTP proxy | [Yes](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-create-api-as-simple-proxy-for-http.html) | [Yes](https://tyk.io/docs/key-concepts/tcp-proxy/) | [Yes](https://docs.konghq.com/2.0.x/proxy/) | [Yes](https://www.express-gateway.io/docs/configuration/gateway.config.yml/http/) |
| TLS Termination | [Yes](https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-custom-domains.html#custom-domain-names-certificates) | 
| JWT | Hard to understand | [Yes](https://tyk.io/docs/basic-config-and-security/security/authentication-authorization/json-web-tokens/) | 
| OAuth2 | No | [Yes](https://tyk.io/docs/basic-config-and-security/security/authentication-authorization/oauth-2-0/) | 
| OIDC | [With Cognito](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-integrate-with-cognito.html) | [Yes](https://tyk.io/docs/basic-config-and-security/security/authentication-authorization/openid-connect/)
| Backend TLS verification | [Yes](https://docs.aws.amazon.com/apigateway/latest/developerguide/getting-started-client-side-ssl-authentication.html) | 
| **Request Routing and Manipulation** |
| Transform inbound request | [Yes](https://docs.aws.amazon.com/apigateway/latest/developerguide/example-photos.html#example-photos-input-mapping) | [Yes](https://tyk.io/docs/advanced-configuration/transform-traffic/) |
| Transform response | [Yes](https://docs.aws.amazon.com/apigateway/latest/developerguide/example-photos.html#example-photos-output-mapping) | [Yes](https://tyk.io/docs/advanced-configuration/transform-traffic/response-body/) | 
| Request Validation | [Yes](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-validation-sample-api-swagger.html) | [Yes](https://tyk.io/docs/advanced-configuration/transform-traffic/validate-json/) |
