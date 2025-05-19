### About Nordsee

_Nordsee_ is a demo program with ocean waves simulation.
All computations are performed on CPU, rendering is CPU-based too.

It works in the following way: waves spectrum is generated, then it is evaluated in time, then water surface heightmap is generated from current spectrum (using inverse FFT). Additionally this heightmap is modified to change waves form - from simple sinwaves to Gerstner waves.

Colors are generated for given water surface heightmap, including simple lighting and a couple of other effects. Then this heightmap is rendered using floating horizon algorithm.


### Controls

* W - move forward
* S - move backward
* A - move left
* D - move right
* Space - move up
* C - move down
* ↑ - turn camera up
* ↓ - turn camera down
* ← - turn camera left
* → - turn camera right
* Z - toggle debug info
* Esc - quit


### How to build

_Nordsee_ is written in [Ü](https://github.com/Panzerschrek/U-00DC-Sprache).
Building it is pretty straightforward - just run `u.._build_system1 build` in order to do this.

SDL2 is required. On GNU/Linux system SDL2 library may be used.
But on Windows you need to provide path to SDL2 installation directory in order to perform the build.
You need to create a file named `configuration_options.json` with contents like this:
```json
{
    "sdl_install_prefix" : "C:/my/SDL2/installation/path"
}
```

Then you need to specify path to this file in command line options:
```
u.._build_system1 build --configuration-options configuration_options.json
```


### Authors
Copyright © 2025 "Panzerschrek".
