# Himeno
The Himeno benchmark [1] version 3.0 is a test program measuring the cpu performance in MFLOPS.Point-Jacobi method is employed in this Pressure Poisson equation solver as this method can be easily vectorized and be parallelized.

The size of this kernel benchmark can be choosen from the following sets of

`[mimax][mjmax][mkmax]:`
`small : 33,33,65`
`small : 65,65,129`
`midium: 129,129,257`
`large : 257,257,513`
`ext.large: 513,513,1025`

## Compilation :
`cc himenobmtxpa.c -O3 -mavx2 -o himenobmtxpa`

Note: Include the CFLAG -mavx2 only if the machine provides AVX2 support (To check AVX2 support use the command : grep avx2 /proc/cpuinfo )

# Execution :
`himenobmtxpa s`

# References :
[1] http://accc.riken.jp/en/supercom/himenobmt, download at http://accc.riken.jp/en/supercom/himenobmt/download/98-source/
