# 4DZip

Verifiable lossless compression and byte-exact restoration of Gatan DigitalMicrograph (.dm4)
4D-STEM files into standard HDF5 (.4dz).
SKKU-STEM Laboratory, Sungkyunkwan University - https://skkustem.org

## Download

The [releases](https://github.com/SKKU-STEM/4dzip/releases) page offers, for Windows 10 and 11
(64-bit, offline, no Python needed):

- `4dzip_v<version>_win64_setup.exe`, a setup wizard for the current user (no administrator rights)
- `4dzip_v<version>_win64_portable.zip`, to use without installation
- `4DZip_User_Manual_v<version>.pdf`, the user manual (also inside both downloads)
- a `.sha256` file for each download and `SHA256SUMS.txt`

## Use

```
4dzip compress scan.dm4          writes scan.4dz (verified before it is renamed)
4dzip verify scan.4dz --source scan.dm4
4dzip restore scan.4dz -o other_folder\scan.dm4
4dzip info scan.4dz
```

Integrity checks are made only by `4dzip verify`. See the manual for details, reading
archives with h5py and hdf5plugin, and the experimental lossy-count copy.

## Source code and data

The source code, the .4dz format specification and a DigitalMicrograph launcher are available
from the corresponding author on request: Young-Min Kim, youngmk@skku.edu.

## Citation

Please cite the paper describing 4DZip.

## License

BSD 3-Clause License (`LICENSE`). Licenses of the bundled components are in
`THIRD_PARTY_LICENSES.txt` inside each download.
