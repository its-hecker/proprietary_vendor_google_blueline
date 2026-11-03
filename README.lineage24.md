# Pixel 3 vendor input for LineageOS 24.0

This dedicated branch starts from the existing `lineage-22.2` vendor commit
`3e448b6d0bff3e6df52473ac9b249f61dc17bb46`. Legacy blob version numbers do not
identify the Android platform being built.

Use this branch through the LineageOS 24.0 Pixel 3 local manifest:
https://github.com/its-hecker/Blueline-Crdroid-Local-Manifest

Before compiling, its build helper applies the matching device tree's extraction
fixups locally and regenerates Android.bp and vendor makefiles. This includes
camera library dependencies, the fingerprint stats interface and the Secure UI
shim. The raw files on this branch are the input to that preparation; building
them directly without the helper does not apply the Android 17 fixups.

Radio images use Git LFS. Complete the LFS-enabled source sync first. No factory
image, ADB connection or phone flashing is performed by vendor preparation.

These sources have not yet been validated by a complete Pixel 3 Android 17 build
and phone test.
