# libheif compiled to WebAssembly (libheif-js 1.23.5)

- Files: `libheif.js` (the Emscripten loader with libheif's JavaScript bindings) and `libheif.wasm`, copied unchanged from
  the npm package `libheif-js@1.23.5` (`libheif-wasm/`). npm integrity:
  `sha512-umXZPthnWZtF3iG/5mQG+AZ2V6i0UeYpo3z2CkggTEgL8dKmIIwJT6TDuAMuabXa1yTW8uJ1ZAgR+CxNTklYYw==`.
- What is inside the WebAssembly:
  - libheif (HEIF and HEIC image decoding), by struktur AG. Licence: LGPL-3.0, `LICENSE-libheif.txt` (libheif's own
    licence file, as shipped in the package).
  - libde265 1.0.15 (the HEVC decoder for HEIC pictures), by struktur AG. Licence: LGPL-3.0, `COPYING-libde265.txt`.
  - Whatever else libheif's `build-emscripten.sh` compiles in by default at that commit (see the script; for example
    OpenJPEG 2.5.4, BSD-2-Clause, when it is enabled).
  - The npm packaging by Kiril Vatev (catdad-experiments). Licence: LGPL-3.0, `LICENSE-libheif-js-LGPL-3.0.txt`.
- Corresponding source:
  - The build: https://github.com/catdad-experiments/libheif-emscripten at tag `v1.23.5` (commit
    5c8968a44e9c68ae677e24790d77d001ed7fe7cc), which builds the libheif submodule with libheif's own scripts, unmodified
    (Emscripten 3.1.61, `USE_WASM=1 USE_UNSAFE_EVAL=0`).
  - libheif: https://github.com/strukturag/libheif at commit 413e2a87e6a70b3eccc3a3adc5801179dd2d9e00.
  - libde265: https://github.com/strukturag/libde265 at tag `v1.0.15`.
  - The npm package: https://github.com/catdad-experiments/libheif-js at tag `1.23.5` and https://www.npmjs.com/package/libheif-js/v/1.23.5
- Replacing the library (LGPL-3.0 section 4): the apps load these two files by URL and check their SHA-256, so a rebuilt
  `libheif.js` and `libheif.wasm` made from the sources above can be served in their place with new checksums.
- Checksums are in `manifest.json`. The apps check the byte length and SHA-256 before running either file.
- Used by: Slopographic File convert (HEIC and HEIF photos to JPG, PNG and WebP), through `shared/heic/` in the apps repo.
