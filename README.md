# interactor-retarget

Intersection-free garment retargeting: it refits a garment authored for one body onto another without the cloth passing through the body.

## What it is for

The solve is a finite-element optimization that respects skeleton correspondence. The C-ABI mesh source and sink contracts in the port library are the boundary the core is moving to; the core still reads and writes its own files. [EXTRACTION.md](EXTRACTION.md) tracks the move of the solver out of its earlier repository.

## Build and run

```sh
cmake -B build
cmake --build build
```

The default build makes the port library alone. `-DWEFTFIT_BUILD_CORE=ON` adds the fetched solver sources and their finite-element substrate.

## Licence

MIT; see LICENSE, which carries the finite-element library's copyright.
