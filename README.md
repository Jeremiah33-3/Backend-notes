# Backend-notes

What is Firebase?
> Firebase is a set of backend cloud computing services and application development platforms provided by Google. It hosts databases, services, authentication, and integration for a variety of applications, including Android, iOS, JavaScript, Node.js, Java, Unity, PHP, and C++.

Helpful resources:
1. Setting up: https://firebase.google.com/docs/web/setup
2. Tutorial: https://youtu.be/fgdpvwEWJ9M
3. Difference between SDK and API: https://www.ibm.com/cloud/blog/sdk-vs-api
4. what is REST API: https://www.ibm.com/topics/rest-apis
5. Supabase: https://supabase.com/docs
6. geeksforgeeks web dev notes: https://www.geeksforgeeks.org/web-development/
7. React's `useEffect`: https://react.dev/reference/react/useEffect
8. Next.js: https://nextjs.org/docs/getting-started/project-structure

MySQL stuffs
1. Tutorial: https://youtu.be/7S_tz1z_5bA
2. Fetching data from a different sql server: https://stackoverflow.com/questions/1144051/selecting-data-from-two-different-servers-in-sql-server


## Authetication

1. Calling API using Authetication code flow
Source:
- https://auth0.com/docs/get-started/authentication-and-authorization-flow/call-your-api-using-the-authorization-code-flow
- https://oauth.net/2/grant-types/authorization-code/
- https://developer.okta.com/blog/2018/04/10/oauth-authorization-code-grant-type
- https://www.oauth.com/oauth2-servers/access-tokens/authorization-code-request/
- OAuth guide/documentation: https://www.oauth.com/oauth2-servers/background/

Main points: 
- for OAuth 2.0 
- granting authorization from third-party provider 
- need redirect URL

2. What is PKCE when we talk about OAuth?

PKCE: Proof key for code exchange.
> OAuth decouples authentication from authorization, by relying on a third party to grant an access token. Doing this reduces your attack surface since your client secret is not required to access certain resources.

One popular grant type = authorization code flow, with JWT as one standard to use this grant type. Authorization Code Flow protects client's secret by redirectly a request for a token through an Authorization Server. 

[Implicit grant](https://datatracker.ietf.org/doc/html/rfc6749#section-1.3.2) is a simplified authorization code flow optimize for clients implemented in a browser using a scripting language such as JavaScript. Client is issued the access token directly instead of authorization code (no intermediate credentials).  
On the other hand, [PKCE](https://oauth.net/2/pkce/) 'is an extension to the Authorization Code flow to prevent certain attacks and to be able to securely perform the OAuth exchange from public clients.”. PKCE is becoming the standard best practise to enhance security. PKCE replaces the client secret used in the standard Authorization Code flow with a one-time code challenge. This means the client app doesn’t have to store a client secret.

Source/Reading:
- https://blog.postman.com/pkce-oauth-how-to/
- https://christianlydemann.com/implicit-flow-vs-code-flow-with-pkce/
- Server-side rendering in Supabase: https://supabase.com/docs/guides/auth/server-side-rendering

3. Supabase auth library 

Source: https://supabase.com/docs/guides/auth/auth-helpers/nextjs

4. Client-side vs server-side authetication flow | session vs token

Source/Reading:
- https://www.yeti.co/blog/client-vs-server-oauth-flows-with-rest-apis
- https://dev.to/thecodearcher/what-really-is-the-difference-between-session-and-token-based-authentication-2o39
- https://stackoverflow.com/questions/43452896/authentication-jwt-usage-vs-session

-- seems like implicit vs PKCE 
