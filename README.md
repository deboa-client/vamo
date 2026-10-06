# Vamo

**vamo** ("let's go" in Brazilian Portuguese) is a DRY REST client wrapper built on top of [deboa](https://crates.io/crates/deboa).

## Install

```toml
vamo = "0.0.1"
deboa-smol = "0.1.0"
```

## Usage

```rust, compile_fail
use vamo::Vamo;

let vamo = Vamo::<deboa_smol::Client>::new("https://api.example.com")?;
let response = vamo
    .get("/users")?
    .send()
    .await?;
```

## Subcrates

### [vamo](https://github.com/deboa-client/vamo/tree/main/vamo)

Nice wrapper on top of deboa for dry rest client. Set base url once
and use it for all requests.

### [vamo-macros](https://github.com/deboa-client/vamo/tree/main/vamo-macros)

Vamo macros is a collection of macros to make possible use structs as resources to be sent over vamo as client.
It is also the new home of bora macro.

## License

Licensed under either of

- Apache License, Version 2.0
  (LICENSE-APACHE or <https://www.apache.org/licenses/LICENSE-2.0>)
- MIT license
  (LICENSE-MIT or <https://opensource.org/licenses/MIT>)

at your option.

## Author

Rogerio Pereira Araujo <rogerio.araujo@gmail.com>
