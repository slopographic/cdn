# slopographic/cdn

Optional files for Slopographic apps (models, font packs, the video engine). Apps download these only when a person chooses them. Each folder has a versioned manifest.json with SHA-256 checksums, and apps check every file before use.

| File | Used by | Licence | Source |
|---|---|---|---|
| models/upscale/realesrgan-x4plus.onnx | Slop Upscale | BSD-3-Clause | xinntao/Real-ESRGAN |
| models/depth/depth-anything-v2-small.onnx | Slop Image to 3D | Apache-2.0 | depth-anything/Depth-Anything-V2-Small |
| packs/barlow/v1/*.ttf | Slop fonts (Get more: Barlow and Barlow Condensed) | OFL-1.1 (see packs/barlow/v1/OFL.txt) | google/fonts ofl/barlow; see packs/barlow/v1/SOURCE.md |
| engines/ffmpeg/0.12.10/ffmpeg-core.wasm (and .js) | Slop Convert (video conversions) | GPL-2.0-or-later (see engines/ffmpeg/0.12.10/LICENSE-GPL-2.0.txt) | ffmpeg.wasm 0.12.10 and FFmpeg; see engines/ffmpeg/0.12.10/SOURCE.md |

SHA-256 values are listed in the apps' model index files and in each folder's manifest.json (for example engines/ffmpeg/0.12.10/manifest.json).
