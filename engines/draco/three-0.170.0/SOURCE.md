# Draco decoder, glTF build (from three.js 0.170.0)

- Files: `draco_wasm_wrapper.js`, `draco_decoder.wasm` and `draco_decoder.js` (the fallback for browsers without WebAssembly), copied unchanged from the npm package `three@0.170.0` (`examples/jsm/libs/draco/gltf/`).
- What it is: Google's Draco mesh decoder, the build for the glTF extension `KHR_draco_mesh_compression`. Used by three.js `DRACOLoader` when a glTF or GLB file has Draco-compressed meshes.
- Licence: Apache-2.0. The licence text is in `LICENSE-Apache-2.0.txt`.
- Source: https://github.com/google/draco (branch `gltf_2.0_draco_extension`), and https://www.npmjs.com/package/three/v/0.170.0
- Checksums are in `manifest.json`. The apps check the SHA-256 before running the file.
