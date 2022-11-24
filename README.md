# mach/glfw OpenGL example

This is an example for how to use [mach-glfw](https://github.com/hexops/mach-glfw) and [zig-opengl](https://github.com/MasterQ32/zig-opengl) together to create a modern OpenGL 4.1 (latest version supported on macOS) window.

## Getting started

### Clone the repository

Cloning submodules is required, so use `--recursive`:

```sh
git clone --recursive https://github.com/hexops/mach-glfw-opengl-example
cd mach-glfw-opengl-example/
```

### Run the example

```sh
zig build run
```

## Next steps

### Understanding this example

This example only clears the screen to a purple color. It doesn't show how to get e.g. triangles onto the screen; you'll need to look at other OpenGL examples for that as a next step. We're happy to accept a PR for this.

### Understanding how zig-opengl works

[zig-opengl](https://github.com/MasterQ32/zig-opengl) provides a binding generator which uses `dotnet` to generate pure-Zig OpenGL bindings. We generate and commit them to this repository for simplicity:

```sh
cd libs/zig-opengl/
mkdir exports/
make
mv exports/gl_4v0.zig ../gl.zig
```

## Getting help

You can join the [Mach discord](https://discord.gg/XNG3NZgCqp) for help if this example doesn't work. Also consider joining the Zig discord's `#gamedev` channel.
