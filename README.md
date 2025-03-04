# A GraphQL server library implemented in Rust

<div align="center">
  <!-- CI -->
  <img src="https://github.com/async-graphql/async-graphql/workflows/CI/badge.svg" />
  <!-- codecov -->
  <img src="https://codecov.io/gh/async-graphql/async-graphql/branch/master/graph/badge.svg" />
  <!-- Crates version -->
  <a href="https://crates.io/crates/async-graphql">
    <img src="https://img.shields.io/crates/v/async-graphql.svg?style=flat-square"
    alt="Crates.io version" />
  </a>
  <!-- Downloads -->
  <a href="https://crates.io/crates/async-graphql">
    <img src="https://img.shields.io/crates/d/async-graphql.svg?style=flat-square"
      alt="Download" />
  </a>
  <!-- docs.rs docs -->
  <a href="https://docs.rs/async-graphql">
    <img src="https://img.shields.io/badge/docs-latest-blue.svg?style=flat-square"
      alt="docs.rs docs" />
  </a>
  <a href="https://github.com/rust-secure-code/safety-dance/">
    <img src="https://img.shields.io/badge/unsafe-forbidden-success.svg?style=flat-square"
      alt="Unsafe Rust forbidden" />
  </a>
</div>

`Async-graphql` is a high-performance server-side library that supports all GraphQL specifications.

* [Feature Comparison](feature-comparison.md)
* [Book](https://async-graphql.github.io/async-graphql/en/index.html)
* [中文文档](https://async-graphql.github.io/async-graphql/zh-CN/index.html)
* [Docs](https://docs.rs/async-graphql)
* [GitHub repository](https://github.com/async-graphql/async-graphql)
* [Cargo package](https://crates.io/crates/async-graphql)
* Minimum supported Rust version: 1.51.0 or later

## Safety

This crate uses `#![forbid(unsafe_code)]` to ensure everything is implemented in 100% Safe Rust.

## Features

* Fully supports async/await
* Type safety
* Rustfmt friendly (Procedural Macro)
* Custom scalars
* Minimal overhead
* Easy integration (actix_web, tide, warp, rocket ...)
* Upload files (Multipart request)
* Subscriptions (WebSocket transport)
* Custom extensions
* Apollo Tracing extension
* Limit query complexity/depth
* Error Extensions
* Apollo Federation
* Batch Queries
* Apollo Persisted Queries

## Crate features

This crate offers the following features, all of which are not activated by default:

- `apollo_tracing`: Enable the [Apollo tracing extension](extensions/struct.ApolloTracing.html).
- `apollo_persisted_queries`: Enable the [Apollo persisted queries extension](extensions/apollo_persisted_queries/struct.ApolloPersistedQueries.html).
- `log`: Enable the [logger extension](extensions/struct.Logger.html).
- `tracing`: Enable the [tracing extension](extensions/struct.Tracing.html).
- `opentelemetry`: Enable the [OpenTelemetry extension](extensions/struct.OpenTelemetry.html).
- `unblock`: Support [asynchronous reader for Upload](types/struct.Upload.html)
- `bson`: Integrate with the [`bson` crate](https://crates.io/crates/bson).
- `chrono`: Integrate with the [`chrono` crate](https://crates.io/crates/chrono).
- `chrono-tz`: Integrate with the [`chrono-tz` crate](https://crates.io/crates/chrono-tz).
- `url`: Integrate with the [`url` crate](https://crates.io/crates/url).
- `uuid`: Integrate with the [`uuid` crate](https://crates.io/crates/uuid).
- `string_number`: Enable the [StringNumber](types/struct.StringNumber.html).
- `dataloader`: Support [DataLoader](dataloader/struct.DataLoader.html).
- `secrecy`: Integrate with the [`secrecy` crate](https://crates.io/crates/secrecy).
- `decimal`: Integrate with the [`rust_decimal` crate](https://crates.io/crates/rust_decimal).

## Apollo Studio

Apollo Studio is a cloud platform that helps you build, monitor, validate, and secure your organization's data graph.
An existing extension is available for this crate [here](https://github.com/async-graphql/async_graphql_apollo_studio_extension)

## Examples

All examples are in the [sub-repository](https://github.com/async-graphql/examples), located in the examples directory.

**Run an example:**

```shell
git submodule update # update the examples repo
cd examples && cargo run --bin [name]
```

## Integrations

* Actix-web [async-graphql-actix-web](https://crates.io/crates/async-graphql-actix-web)
* Warp [async-graphql-warp](https://crates.io/crates/async-graphql-warp)
* Tide [async-graphql-tide](https://crates.io/crates/async-graphql-tide)
* Rocket [async-graphql-rocket](https://github.com/async-graphql/async-graphql/tree/master/integrations/rocket)
* Axum [async-graphql-axum](https://github.com/async-graphql/async-graphql/tree/master/integrations/axum)

## Blog Posts

- [GraphQL in Rust](https://romankudryashov.com/blog/2020/12/graphql-rust/)

- [How to implement a Rust micro-service using Rocket, GraphQL, PostgreSQL](https://lionkeng.medium.com/how-to-implement-a-rust-micro-service-using-rocket-graphql-postgresql-a3f455f2ae8b)

- [Running GraphQL on Lambda with Rust](https://dylananthony.com/posts/graphql-lambda-rust)

## License

Licensed under either of

* Apache License, Version 2.0,
  ([LICENSE-APACHE](./LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
* MIT license ([LICENSE-MIT](./LICENSE-MIT) or http://opensource.org/licenses/MIT)
  at your option.

## References

* [GraphQL](https://graphql.org)
* [GraphQL Multipart Request](https://github.com/jaydenseric/graphql-multipart-request-spec)
* [GraphQL Cursor Connections Specification](https://facebook.github.io/relay/graphql/connections.htm)
* [GraphQL over WebSocket Protocol](https://github.com/apollographql/subscriptions-transport-ws/blob/master/PROTOCOL.md)
* [Apollo Tracing](https://github.com/apollographql/apollo-tracing)
* [Apollo Federation](https://www.apollographql.com/docs/apollo-server/federation/introduction)

## Contribute

Welcome to contribute !
