# Rosetta hashes for macOS 27.3 beta (26C5035r)

Adds this build's Rosetta `runtime` and `libRosettaRuntime` hashes as second
allowed values in `syscallAbiSupported`, so the syscall dispatch turns on.
The five emitter guards (`0x193f4`, `0x2ace0`, `0x2d4f8`, `0x1996c`, `0x19aec`)
match on this build. See issue #11.

Apply to the patched source that `syscall-dispatch/build.py` produces
(`<output>/source`), then rebuild:

```sh
patch -p1 -d <output>/source < rosetta-26C5035r.patch
cmake --build <output>/build --target runtime_loader libRuntimeRosettax87
```
