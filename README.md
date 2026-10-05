# interactor-retarget

Intersection-free garment retargeting: it refits a garment authored for one body onto another without the cloth passing through the body.

## What it is for

The solve is a finite-element optimization that respects skeleton correspondence. The core never reads or writes files: every mesh crosses the boundary through C-ABI source and sink contracts that adapters implement, so one solve can feed several outputs. [EXTRACTION.md](EXTRACTION.md) tracks the move of the solver out of its earlier repository.

## Build and run

```sh
cmake -B build
cmake --build build
```

The default build makes the port library alone. An option in `CMakeLists.txt` adds the solver core, which fetches its finite-element substrate.

## Licence

MIT; see LICENSE, which carries the finite-element library's copyright.
