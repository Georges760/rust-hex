# hex

[![ga-svg]][ga-url]
[![crates-svg]][crates-url]
[![docs-svg]][docs-url]
[![msrv-svg]][msrv-url]
[![codecov-svg]][codecov-url]
[![deps-svg]][deps-url]

[ga-svg]: https://github.com/KokaKiwi/rust-hex/workflows/build/badge.svg
[ga-url]: https://github.com/KokaKiwi/rust-hex/actions
[crates-svg]: https://img.shields.io/crates/v/hex.svg
[crates-url]: https://crates.io/crates/hex
[docs-svg]: https://docs.rs/hex/badge.svg
[docs-url]: https://docs.rs/hex
[msrv-svg]: https://img.shields.io/badge/rustc-1.36+-blue.svg
[msrv-url]: https://blog.rust-lang.org/2019/07/04/Rust-1.36.0.html
[codecov-svg]: https://img.shields.io/codecov/c/github/KokaKiwi/rust-hex
[codecov-url]: https://codecov.io/gh/KokaKiwi/rust-hex
[deps-svg]: https://deps.rs/repo/github/KokaKiwi/rust-hex/status.svg
[deps-url]: https://deps.rs/repo/github/KokaKiwi/rust-hex

Encoding and decoding data into/from hexadecimal representation.

## Examples

Encoding a `String`

```rust
let hex_string = hex::encode("Hello world!");

println!("{}", hex_string); // Prints "48656c6c6f20776f726c6421"
```

Decoding a `String`

```rust
let decoded_string = hex::decode("48656c6c6f20776f726c6421");

println!("{}", decoded_string); // Prints "Hello world!"
```

You can find the [documentation](https://docs.rs/hex) here.

## Installation

In order to use this crate, you have to add it under `[dependencies]` to your `Cargo.toml`

```toml
[dependencies]
hex = "0.4"
```

By default this will import `std`, if you are working in a
[`no_std`](https://rust-embedded.github.io/book/intro/no-std.html)
environment you can turn this off by adding the following

```toml
[dependencies]
hex = { version = "0.4", default-features = false }
```

## Features

- `std`:
  Enabled by default. Add support for Rust's libstd types.
- `alloc`:
  Enabled by default. Add support for alloc types (e.g. `String`) in `no_std` environment.
- `serde`:
  Disabled by default. Add support for `serde` de/serializing library.
  See the `serde` module documentation for usage.

## License

Licensed under either of

- Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
- MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally
submitted for inclusion in the work by you, as defined in the Apache-2.0
license, shall be dual licensed as above, without any additional terms or
conditions.
