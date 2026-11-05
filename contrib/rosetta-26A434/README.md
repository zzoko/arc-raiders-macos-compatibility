# Rosetta hashes for macOS 27.0.1 (26A434)

Adds this build's Rosetta `runtime` and `libRosettaRuntime` hashes as second
allowed values in `syscallAbiSupported`, so the alpha12 syscall dispatch turns on.

Apply to the patched source that `syscall-dispatch/build.py` produces
(`<output>/source`), then rebuild:

```sh
patch -p1 -d <output>/source < rosetta-26A434.patch
cmake --build <output>/build --target runtime_loader libRuntimeRosettax87
```
