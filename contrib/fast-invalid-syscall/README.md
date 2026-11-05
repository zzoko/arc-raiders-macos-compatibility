# Fast path for the invalid-syscall probe

Patch for `Support/source/compatibility/cpu` (identical in all four alpha11.1 zips).
Apply from the folder that contains `Support/`:

```sh
patch -p1 < fast-invalid-syscall.patch
```

Then rebuild `runtime_loader` and `libRuntimeRosettax87` as described in
`Support/source/README.md`. Nothing changes unless `ARC_FAST_INVALID_SYSCALL=1`
is set in the game's environment.
