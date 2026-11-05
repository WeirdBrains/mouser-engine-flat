# The flat engine

Example custom Mouser rendering engine ("flat"): CPU raster presented with softbuffer.

## Install

Mouser ships with it. To install or update it yourself:

```sh
mouser engine install flat
mouser engine install gh:WeirdBrains/mouser-engine-flat
mouser engine use flat
```

Or in Mouser: `esc :ei flat`.

## How it works

A `cdylib` on the [Mouser engine ABI](https://github.com/WeirdBrains/mouser-engine-abi) (v2),
loaded by Mouser at start. If it fails or crashes, Mouser falls back to the next engine and
finally to its basic CPU renderer ([engines](https://github.com/WeirdBrains/mouser/blob/main/docs/engines.md)). The release
archive holds the library and an `engine.toml` naming it.
