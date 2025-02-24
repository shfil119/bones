# bones
pre-built coreboot (4.18) images and documentation on how to flash them for fm2, fm2+, am1 motherboards 

# Goal
Allowing easy access to prebuild images. Be aware that support for these boards was removed from coreboot releases 4.19. Using these images can cause security problems.

# Images for officially supported motherboards by Coreboot 4.18
* Asus A88XM-E (26a13e5ef685f1b286e9461032596565)
* Asus F2A85-M (3429bbdfc9b33192decb58129dd25ac9)
* Asus F2A85-M PRO (d5c4063493bd9f4c1cb4f3cfd0a173f8)
* Asus F2A85-M LE (d0301488b4d06124a6fcc6f9e5aa58e0)
* Msi FM2-A75MA-E35 (0f6e499c2e51ded3774c9f5c0d47282e)

# Limitations
Currently images don't include vrom, this means that dedicated gpu is required. 

USB 3.0 port as USB 2.0.

TurboBoost not working.

# Building on your own

```
make crossgcc-i386 CPUS=$(nproc)
make nconfig 
make -j$(nproc)
```
