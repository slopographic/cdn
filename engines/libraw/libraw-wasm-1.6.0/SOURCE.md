# LibRaw 0.22.1 compiled to WebAssembly (libraw-wasm 1.6.0)

- Files: `libraw.js` (the Emscripten loader with the wrapper's bindings) and `libraw.wasm`, copied unchanged from the npm
  package `libraw-wasm@1.6.0` (`dist/`). npm integrity: `sha512-VfvWq2XGGkc07wexymRLn1H82j6smmC1LAbVl41vnW2Z5RrEPLN+YHi1Hmga2TbxxrY4rOjmTwHwSyTZmypE1g==`.
- What is inside the WebAssembly:
  - LibRaw 0.22.1 (raw photo decoding). Licence: LGPL-2.1 or CDDL-1.0, at your choice. Texts: `LICENSE-LibRaw-LGPL-2.1.txt`,
    `LICENSE-LibRaw-CDDL-1.0.txt`, and `COPYRIGHT-LibRaw.txt` (LibRaw's own statement, which also credits dcraw by Dave Coffin and
    the DCB and FBDD code by Jacek Gozdz).
  - Little CMS 2.19.1 (colour management). Licence: MIT, `LICENSE-LittleCMS-MIT.txt`.
  - libjpeg from the Emscripten ports (lossy DNG and Kodak JPEG raw). This software is based in part on the work of the
    Independent JPEG Group.
  - The wrapper (`libraw_wrapper.cpp`) and the build scripts by ybouane and contributors. Licence: ISC, `LICENSE-libraw-wasm-ISC.txt`.
- Corresponding source:
  - Wrapper and build script (`compileLibraw.sh` pins LibRaw 0.22.1 and lcms2.19.1): https://github.com/ybouane/LibRaw-Wasm at tag
    `v1.6.0` (commit 32fd36a9883a10c1632bc20073f1ea88cc60487a).
  - LibRaw: https://github.com/LibRaw/LibRaw at tag `0.22.1`, and https://www.libraw.org/download
  - Little CMS: https://github.com/mm2/Little-CMS at tag `lcms2.19.1`.
  - The npm package: https://www.npmjs.com/package/libraw-wasm/v/1.6.0
- Replacing the library (LGPL-2.1 section 6): the apps load these two files by URL and check their SHA-256, so a rebuilt
  `libraw.js` and `libraw.wasm` made from the sources above can be served in their place with new checksums.
- Checksums are in `manifest.json`. The apps check the byte length and SHA-256 before running either file.
- Used by: Slopographic PhotoSlop, Slop Gallery, Slop Resize and File convert (camera RAW files), through `shared/raw/` in the apps repo.
