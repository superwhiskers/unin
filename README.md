# numX [![Build Status](https://travis-ci.org/AnyTimeTraveler/numX.svg?branch=master)](https://travis-ci.org/AnyTimeTraveler/numX) [![Crates.io](https://img.shields.io/crates/v/numx.svg)](https://crates.io/crates/numx)

> Non standard integer types like `u122`, `u9`, `i67`, `u10`, `u63`, `i7`, `i9` etc


```rust
struct Packet {
    header: u3,
    timestamp: u5,
    hash: u4,
    mode: u2,
}
```

### This is a fork of [uX](https://github.com/kjetilkjeka/uX) by [kjetilkjeka](https://github.com/kjetilkjeka)

I have merely merged the pull requests on this fork and added features what would otherwise have been my pull request to him.

I am still a rust beginner.
Examine this yourself before deciding to use it!

## Features

When non-standard-width integers is required in an application, the norm is to use a larger container and make sure the value is within range after manipulation.
numX aims to take care of this once and for all by:
 - Providing `u1`-`u127` and `i1`-`i127` types that should behave as similar as possible to the built in rust types
     - The methods of the defined types are the same as for the built in types (far from all is implemented at this point but fill out an issue or create a PR if something essential for you is missing)
     - Overflow will panic in debug and wrap in release.
 - All possible lossless conversions are possible by using `From`.
 - All possible lossy conversions are possible by using `TryFrom`.
 - Support for `serde` by serializing into the next bigger container.
 - All possible conversions to `isize` and `usize` for the target architecture.
 - Implementations of some `num-traits`.

## Thanks

Thank to all the contributors from the original project and to the people who sent the pull requests that I merged:
 - [adamnemecek](https://github.com/adamnemecek)
 - [Atul Bhosale](https://github.com/Atul9)
 - [Kevin Boos](https://github.com/kevinaboos)
 - [Angelo Bulfone](https://github.com/boomshroom)
 - [meh](https://github.com/meh)


## License

Licensed under either of

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or
  http://www.apache.org/licenses/LICENSE-2.0)

- MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

## Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.
