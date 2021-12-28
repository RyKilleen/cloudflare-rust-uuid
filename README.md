# Quickstart

Currently works on Linux/WSL out of the box, [Perl a required Cloudflare dependency on Windows](https://developers.cloudflare.com/workers/cli-wrangler/install-update)

1. `cargo install wrangler`
2. `wrangler dev`
3. http://localhost:8787/uuid
4. http://localhost:8787/uuid/100

For a preview, visit https://cf-worker-test.rykilleen.workers.dev/uuid/1000
___


# Getting Started

A template for kick starting a Cloudflare worker project using [`workers-rs`](https://github.com/cloudflare/workers-rs).

This template is designed for compiling Rust to WebAssembly and publishing the resulting worker to 
Cloudflare's [edge infrastructure](https://www.cloudflare.com/network/).

## Usage 

This template starts you off with a `src/lib.rs` file, acting as an entrypoint for requests hitting
your Worker. Feel free to add more code in this file, or create Rust modules anywhere else for this
project to use. 

With `wrangler`, you can build, test, and deploy your Worker with the following commands: 

```bash
# compiles your project to WebAssembly and will warn of any issues
wrangler build 

# run your Worker in an ideal development workflow (with a local server, file watcher & more)
wrangler dev

# deploy your Worker globally to the Cloudflare network (update your wrangler.toml file for configuration)
wrangler publish
```

Read the latest `worker` crate documentation here: https://docs.rs/worker

## WebAssembly

`workers-rs` (the Rust SDK for Cloudflare Workers used in this template) is meant to be executed as 
compiled WebAssembly, and as such so **must** all the code you write and depend upon. All crates and
modules used in Rust-based Workers projects have to compile to the `wasm32-unknown-unknown` triple. 

Read more about this on the [`workers-rs` project README](https://github.com/cloudflare/workers-rs).

## Issues

If you have any problems with the `worker` crate, please open an issue on the upstream project 
issue tracker on the [`workers-rs` repository](https://github.com/cloudflare/workers-rs).

