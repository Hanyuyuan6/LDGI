# Loop Differential Ghost Imaging Based on Line Pattern

Published paper: [Loop differential ghost imaging based on line pattern](https://doi.org/10.1016/j.optcom.2025.131589) (Optics Communications, 2025).

MATLAB research code for loop differential ghost imaging (LDGI) with optical-phased-array line patterns.

## Requirements

- MATLAB with Image Processing Toolbox and Signal Processing Toolbox (for `sinc`).
- The scripts use an authorized local target image. Set `LDGI_TARGET_IMAGE` to a file path; otherwise they fall back to MATLAB's local `cameraman.tif` sample. Images are resized to 64x64 for the released experiment geometry.

```matlab
setenv('LDGI_TARGET_IMAGE', fullfile(pwd, 'my_target.png'));
```

No target or result TIFF is redistributed by this repository. The removed files and their integrity hashes are documented in [ASSET_PROVENANCE.md](ASSET_PROVENANCE.md).

## Project structure

- `Loop_differential_ghost_imaging/OPA_Speckle_patterns/`: simulations for OPA illumination patterns.
- `Loop_differential_ghost_imaging/oneD_OPA_plus_grating_scanning_imaging_optimize/`: LDGI reconstruction and comparison scripts.

From the repository root in MATLAB, run the LDGI reconstruction example:

```matlab
run(fullfile(pwd, ...
    'Loop_differential_ghost_imaging', ...
    'oneD_OPA_plus_grating_scanning_imaging_optimize', ...
    'op_succeed_FOR_PAPER.m'));
```

## Citation

If this code is useful, cite:

```bibtex
@article{han2025loop,
  title   = {Loop differential ghost imaging based on line pattern},
  author  = {Han, Yuyuan and Zheng, Huaibin and Li, Bin and Li, Jingwei and Qiu, Long and Hao, Wenxuan and Dang, Zheng and Chen, Hui and Liu, Jianbin and He, Yuchen and Liu, Yanyan and Xu, Zhuo},
  journal = {Optics Communications},
  volume  = {580},
  pages   = {131589},
  year    = {2025},
  doi     = {10.1016/j.optcom.2025.131589}
}
```

## Rights

The repository currently does not grant an open-source license for the author-owned MATLAB code. Public visibility is not a license. See [NOTICE.md](NOTICE.md) and [ASSET_PROVENANCE.md](ASSET_PROVENANCE.md).
