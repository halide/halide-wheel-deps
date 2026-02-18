# halide-wheel-deps

A uv workspace that packages third-party C++ dependencies
of [Halide](https://github.com/halide/Halide) as Python wheels
using [scikit-build-core](https://github.com/scikit-build/scikit-build-core).

## Packages

| Package              | Upstream                                                    | Description                                                                  |
|----------------------|-------------------------------------------------------------|------------------------------------------------------------------------------|
| `halide-flatbuffers` | [google/flatbuffers](https://github.com/google/flatbuffers) | Memory-efficient serialization library used by Halide's serialization format |
| `halide-wabt`        | [WebAssembly/wabt](https://github.com/WebAssembly/wabt)     | WebAssembly binary toolkit used by Halide's WebAssembly backend              |

## Building

This project uses [uv](https://docs.astral.sh/uv/)
and [scikit-build-core](https://github.com/scikit-build/scikit-build-core).
CMake 3.28+ is required.

Initialize submodules before building:

```sh
git submodule update --init --recursive
```

Build a specific package:

```sh
uv build --package halide-flatbuffers
uv build --package halide-wabt
```