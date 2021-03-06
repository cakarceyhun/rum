# Rum

## About

Rum is an experiment. It was started with the goal of creating a framework that
can be used to write HTML5 games in [Rust](http://rust-lang.org) via
[Emscripten](http://emscripten.org). Unfortunately I had to realize that my
available time is too limited to reach that goal, so for now, I have to settle
one creating a proof-of-concept that shows it's possible to compile Rust code
to JavaScript with Emscripten.

All of this is pretty raw at the moment. It has only been tested on recent
versions of Ubuntu (64 bit).


## Prerequisites

You need a working [node.js](http://nodejs.org). I've tested with v0.10.26, but
I don't think this is very much version-specific.

You'll also need some basics to build Rust and LLVM: make, a C/C++ compiler,
that kind of stuff. If you run into any problems, feel free to add your
solutions to this README and send me a pull request!

This repository includes Rust, Emscripten and LLVM, so you're covered on that
front.


## Usage

Before using this the first time, you need to initialize the repository:

> $ ./scripts/init

Be aware: This will take a while.

After that, you can compile and run the Rust program (source/main.rs) with the
following command:

> $ ./scripts/run


## Limitations

As you can see, currently the Rust program is very basic, kind of a
proto-"Hello, World". The reason for this is that currently, only programs that
don't require any kind of Rust library (including std) will run. Trying to write
an actual "Hello, World" (i.e. using a string) already requires the std.

As soon as I have some time to invest in this again, I will try to overcome this
limitation and support "real" Rust programs.
