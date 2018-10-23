# hello-esy-dune-bsb

Let's try to compile OCaml to JavasScript using
[Esy](https://esy.sh),
[Dune](https://dune.build/)
and [BuckleScript](https://bucklescript.github.io).

*NOTE: This an experimental package to test building BuckleScript projects with Dune.*
It won't work until Dune supports building with Bucklescript.
You can follow along with progress in the [BuckleScript issue](https://github.com/ocaml/dune/issues/140) in the Dune repo,
and the [bucklescript branch](https://github.com/ocaml/dune/tree/bucklescript) of Dune.

## Installation

You will need to have `esy` command installed:

```sh
npm install -g esy # or yarn global add esy
```

Then run `esy` in this directory to install dependencies and attempt a build.

```sh
esy
```

Right now this build probably will not succeed as work is still underway to support BuckleScript in Dune.
However, once the dependencies are installed we can build the project with BuckleScript.

```sh
esy build:bsb
```

This will produce some verbose build output,
some build artifacts in `lib/` which may be of interest,
and the compiled JavaScript file `bin/hello.bs.js`.
