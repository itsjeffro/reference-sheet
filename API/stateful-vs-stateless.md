# Stateful vs Stateless

Sources:

- https://www.redhat.com/en/topics/cloud-native-apps/stateful-vs-stateless

## Stateful

A typical application may send the user's session with each request.

For example, a typical login will usually store a cookie after a successful login. But if the application used API's but relied on the user's stored cookie with each subsequent request, this woud be considered an "stateful API".

**Things to consider:**

- We should still be cautious of CSRF attacks even if the application takes a stateful API approach. Once the user is redirected from a malicious site back to the original application, the user's cookie will be present with the request and causing an unwanted action.

## Stateless

TBD
