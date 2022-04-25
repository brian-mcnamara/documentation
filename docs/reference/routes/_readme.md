---
id: routes
title: Routes
keywords:
- reference
- Routes
---


# Routes
- Environment Variable: `ROUTES`
- Config File Key: `routes`
- Type: [base64 encoded] `string` or inline policy structure in config file
- **Required** - While Pomerium will start without a route configured, it will not authorize or proxy any traffic until a route is defined. If configuring Pomerium for the Enterprise Console, define a route for the Console itself in Pomerium.

A route contains specific access and control definitions for a back-end service. Each route is a list item under the `routes` key.

Each route defines at minimum a `from` and `to` field, and a `policy` key defining authorization logic. Policies are defined using [Pomerium Policy Language](/enterprise/reference/manage.md#pomerium-policy-language) (**PPL**). Additional options are listed below.

<<< @/examples/config/route.example.yaml
