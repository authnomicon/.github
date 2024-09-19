## Authnomicon

The Authnomicon project is a reference implementation of various [identity and
access management](https://en.wikipedia.org/wiki/Identity_management) (IAM)
standards and protocols.

This project provides components that implement web-based authentication,
[session management](https://en.wikipedia.org/wiki/HTTP#HTTP_session), [single
sign-on](https://en.wikipedia.org/wiki/Single_sign-on) (SSO) via [OpenID](https://en.wikipedia.org/wiki/OpenID)
and [SAML](https://en.wikipedia.org/wiki/Security_Assertion_Markup_Language),
delegated authorization via [OAuth](https://en.wikipedia.org/wiki/OAuth), and
provisioning via [SCIM](https://en.wikipedia.org/wiki/System_for_Cross-domain_Identity_Management).

These components are implemented for [Bixby.js](https://github.com/bixbyjs), a
dependency injection framework for [Node.js](https://nodejs.org/) applications.
This allows the project to provide protocol endpoints independent of
application-specific business logic.  Business logic is injected into and driven
by protocol implementations in accordance with [hexagonal architecture](https://en.wikipedia.org/wiki/Hexagonal_architecture_(software)).

The result is a fully-functional IAM system, where business logic components can
be swapped out and replaced according to application-specific needs, while still
leveraging the protocol implementations.

[Read more &rarr;](https://github.com/authnomicon/.github#overview)
