# unin

a maintained, hard-forked implementation of integers in nonstandard widths for rust programs

## fork information

this is forked from [numX](https://github.com/AnyTimeTraveler/numX), which is itself forked from
[uX](https://github.com/kjetilkjeka/uX). the reasoning behind this is that neither have been
updated for over a year (uX for over two years,) and i would like to be able to make upstreamable
changes quicker than pull requests would allow

## features

 - `u1`-`u127` and `i1`-`i127` types that should behave as similar as possible to the built in rust
   types (some methods may be missing. i plan to attempt to fix this)
 - lossless conversions implemented under the `From` trait
 - lossy conversions implemented under the `TryFrom` trait
 - support for `serde` by serializing into the next biggest container
 - implementations of conversions to `isize` and `usize` for the target architecture
 - implementations of some traits provided by `num-traits`

## credits

i wouldn't typically include such a section, but in the spirit of the numX fork, here are the
people who i've included contributions from

 - [adamnemecek](https://github.com/adamnemecek)
 - [Atul Bhosale](https://github.com/Atul9)
 - [Kevin Boos](https://github.com/kevinaboos)
 - [Angelo Bulfone](https://github.com/boomshroom)
 - [meh](https://github.com/meh)
 - [Simon Struck](https://github.com/AnyTimeTraveler)

## licensing information

this crate is licensed under either of the following

- [apache license](license-apache)
- [mit license](license-mit)

## contribution

unless explicitly stated otherwise, any contribution intentionally submitted for inclusion in the
work by you, as defined in the Apache-2.0 license, shall be dual licensed as above, without any
additional terms or conditions.
