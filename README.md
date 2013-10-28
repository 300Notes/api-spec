# API Specification

<img src="https://raw.github.com/300Notes/api-spec/master/img/logo.png" alt="300 Notes" align="right" width=200/>

This is a complete specification of all available endpoints, resource types, and authenticated request workflow.

### Endpoints
The **`auth`** namespace provides client token generation and convenience methods for locating canonical session
resources.
 - [`/auth/profile`](auth/profile.md)
 - [`/auth/token`](auth/token.md)

The **`profiles`** namespace provides individual account details.
 - [`/profiles/{id}`](profiles/single.md)

### Resources
Resources are objects that are reused throughout the API. In client libraries, they are often referred to as "models",
"entities", or "documents".
 - [Error](resources/error.md)
 - [Profile](resources/profile.md)
 - [Token](resources/token.md)

### Workflow
The workflow documentation can help you get started with certain aspects of the API.
 - [Authenticated](workflow/auth.md)
