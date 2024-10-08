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

### Overview

#### Authentication

- [@authnomicon/prompts](https://github.com/authnomicon/prompts) - Components to
  present prompts to the user in a web browser, as part of a challenge-response
  flow needed to obtain authentication and authorization.

- [@authnomicon/login](https://github.com/authnomicon/login) - Components for
  prompting a user to log in, as well as authenticating using a password
  credential.
  
- [@authnomicon/federated](https://github.com/authnomicon/federated) -
  Components for federated identity operations (single sign-on (SSO), single
  logout (SLO), delegated authorization) with external identity providers
  (IDPs).

- [@authnomicon/oob](https://github.com/authnomicon/oob) - Components for
  out-of-band authentication, including email magic link and SMS one-time
  password (OTP).

#### Session Management

- [@authnomicon/session](https://github.com/authnomicon/session) - Components
  for maintaining authentication context during a web-based login session.

#### Federation

- [@authnomicon/oauth2](https://github.com/authnomicon/oauth2) - Components for
  building an OAuth 2.0 authorization server (AS) and providing authorization to
  third-party applications.
  
- [@authnomicon/openidconnect](https://github.com/authnomicon/openidconnect) -
  Components for building an OpenID Connect provider (OP) and providing
  authentication to relying party (RP) applications.

#### Directory Services

- [@authnomicon/postgresql](https://github.com/authnomicon/postgresql) -
  Components that provide data access and persistence for user profile
  information and credentials using PostgreSQL.
