# hello-esy-dune-bsb

Let's try to compile OCaml to JavasScript using
[Esy](https://esy.sh),
[Dune](https://dune.build/)
and [BuckleScript](https://bucklescript.github.io).

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
./node_modules/.bin/bsb -make-world -clean-world -verbose
```

This will produce some verbose build output,
some build artifacts in `lib/` which may be of interest,
and the compiled JavaScript file `bin/hello.bs.js`.
