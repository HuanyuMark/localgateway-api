# localgateway-api

Rust crate `localgateway-api`: the LocalGateway management API client, generated
from the LocalGateway OpenAPI contract with openapi-generator 7.26.0.

The generated sources under `src/` must not be edited by hand; runtime
adaptations live in the separate `localgateway-sdk` crate.

## Usage

```toml
[dependencies]
localgateway-api = { git = "https://github.com/HuanyuMark/localgateway-api", tag = "v0.1.0", default-features = false }
```

TLS is disabled by default because the client only talks to the loopback
gateway; enable the `native-tls` or `rustls` feature when needed.