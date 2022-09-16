# Stateful VS Stateless

Sources:

- https://www.redhat.com/en/topics/cloud-native-apps/stateful-vs-stateless

### Stateful

A typical application may send the user's session with each request.

For example, a typical login will usually store a cookie after a successful login. But if the application used API's but relied on the user's stored cookie with each subsequent request, this woud be considered an "stateful API".
