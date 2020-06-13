# YEW DevEnv

[![Built With: RUST](https://img.shields.io/badge/Built%20With-RUST-lightgrey)](https://www.rust-lang.org/) [![WASM: Yew](https://img.shields.io/badge/WASM-Yew-brightgreen)](https://yew.rs/) [![License: Unlicense](https://img.shields.io/badge/license-UNLICENSE-green)](https://unlicense.org)

Yew Development Environment (Rust + Yew + Node + Rollup)

## Usage

Just run the `run` script; it should correctly initialize the environment at the first run (both cargo and npm)

```bash
./run
```

Make sure to customize both _Cargo.toml_ and _package.json_

Moreover, if you rename the project/folder accordingly, you have to remeber to change also the filenames in _main.js_

In short: wherever you see `"yew-devenv"`, `yew_devenv.js` or `yew_devenv_bg.wasm` you have to substitute with the name of your project (example if the first becomes `"awesome-project"`, you have to substitute in _main.js_ also `awesome_project.js` and `awesome_project_bg.wasm` respectively)

### Caveat: Cleanup

Sometimes the hot-reload server or the `thttp` server just stay up, while building fails, etc.
In case of "zombie" servers, try to fix it with `--clean`

```bash
./run --clean
```

## The Environment

The environment is as such:

- Rust package managing through [Cargo](https://github.com/rust-lang/cargo)
- JavaScript package managing through [NPM](https://www.npmjs.com/)
- Rust-WASM binds through [Wasm-Pack](https://rustwasm.github.io/wasm-pack/) and [web-sys](https://rustwasm.github.io/wasm-bindgen/web-sys/index.html)
- JS packer through [rollup](https://rollupjs.org/)
- dev-server though [thttp](https://crates.io/crates/thttp)
- hot-reload though [cargo watch](https://crates.io/crates/cargo-watch) and [rollup-plugin-livereload](https://www.npmjs.com/package/rollup-plugin-livereload)

## LICENSE

**Copyleft 2020, Davide Del Papa**

This repo is under the [unlicense](https://unlicense.org) license. Substitute the license in your own project at will.

May God bless you.
