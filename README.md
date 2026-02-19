# Vimmerse API Documentation

This repository contains the [Fern](https://buildwithfern.com) configuration for the Vimmerse API documentation site.

## Prerequisites

Install the Fern CLI:

```bash
npm install -g fern-api
```

## Project structure

```
fern/
├── fern.config.json       # Organization name and CLI version
├── generators.yml         # Points to the OpenAPI spec
├── docs.yml               # Docs site configuration (navigation, colors, branding)
├── swagger.json           # Vimmerse OpenAPI 3.1 specification
└── pages/
    ├── introduction.mdx   # API overview
    ├── authentication.mdx # Authentication guide
    └── quickstart.mdx     # Getting started tutorial
```

## Commands

### Validate the configuration

```bash
fern check
```

### Preview locally

```bash
fern docs dev
```

This starts a local dev server so you can preview changes before publishing.

### Generate a preview link

```bash
fern generate --docs --preview
```

Creates a shareable preview URL hosted by Fern.

### Publish to production

```bash
fern generate --docs
```

Publishes the docs to `vimmerse.docs.buildwithfern.com`.

## Making changes

- **API spec** — Update `fern/swagger.json`. The API Reference pages are auto-generated from this file.
- **Guides & pages** — Edit or add `.mdx` files in `fern/pages/`, then reference them in `fern/docs.yml` under `navigation`.
- **Branding & layout** — Edit `fern/docs.yml` to change colors, logos, navbar links, or navigation structure.

## Resources

- [Fern documentation](https://buildwithfern.com/learn)
- [docs.yml reference](https://buildwithfern.com/learn/docs/configuration/site-level-settings)
- [Navigation configuration](https://buildwithfern.com/learn/docs/configuration/navigation)
- [OpenAPI generators.yml reference](https://buildwithfern.com/learn/api-definitions/openapi/generators-yml-reference)
