# Supabase notes

## Auth docs
- https://supabase.com/docs/guides/auth

Two parts to Auth system 
1. Authetication (should someone be allowed in, and who are they?)
2. Authorisation (what are they allowed to do?)

- thirdparty providers allowed
- sign in with [enterprise SSO](https://supabase.com/docs/guides/auth/sso/auth-sso-saml) (terminologies at the bottom)
- environment var: name/value pair that can affect the way running processes or programs behave on a computer


## hooks

Reources:
- https://en.wikipedia.org/wiki/Hooking
- https://stackoverflow.com/questions/467557/what-is-meant-by-the-term-hook-in-programming

Essentailly, hook is a place in code/function that: 
- allows one to tap into a module to provide different behaviours or to react when something happens
- intercept function calls and message or events passed between software components 
- able to add new funcitonalities to the programme and change some behaviours 
- able to debug 

**E.g. React custom hooks**
_for creating and customising hook to use_

Sources: 
- https://react.dev/learn/reusing-logic-with-custom-hooks
- https://legacy.reactjs.org/docs/hooks-custom.html
- https://www.youtube.com/watch?v=6ThXsUwLWvc
