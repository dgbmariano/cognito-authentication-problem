
1. Follow this guide to configure Cognito in AWS: https://guides.micronaut.io/micronaut-oauth2-cognito/guide/index.html
2. When modifying the app Settings, set this configurations:
![image](https://user-images.githubusercontent.com/55102164/90302073-1a7d0a00-de7a-11ea-9c74-ad71474dd7b7.png)
3. You will need to create a new Google OAuth 2.0 Client:
![image](https://user-images.githubusercontent.com/55102164/90302089-4d270280-de7a-11ea-8381-b4b1d63b7934.png)
4. Now replace the `client-id`, `client-secret` and the necessary fields in issuer in the `application.yml`.
5. Run the application and open http://localhost:8080/
6. Click in Enter
7. After sign in with Google, the authentication will fail with the message:
```
{"message":"JWT validation failed","_links":{"self":{"href":"/oauth/callback/cognito?code=xxxxxx....","templated":false}}}
```
8. Go back to http://localhost:8080/ and click in Enter again. The authentication will be successful now.
