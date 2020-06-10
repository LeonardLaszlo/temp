# NW.js ARMv7 binaries

### Instructions for running your NW.js application on Linux ARMv7

Executable binaries are available for download under the [Releases][1] tab.

After downloading the binary archive and unpacking it you can run NW.js on Linux ARMv7 devices with the following command:

`./nw --use-gl=egl --ignore-gpu-blacklist --disable-accelerated-2d-canvas --num-raster-threads=2`

### Docker

Building NW.js requires a bunch of resources.
The build was done with a new installation of Docker.
Use as many CPU cores as possible and at least 10 GB of RAM, 4GB swap and 100 GB of disk.

``` Bash
docker image build -t laslaul/nwjs-arm-build-env:v0.45.x .
```

Start the environment:

``` Bash
docker run -it laslaul/nwjs-arm-build-env:v0.45.x
```

Thanks **@gripped**, **@jtg-gg** and **llamasoft**!

### Further reading

Building NW.js on supported platforms [tutorial][4]

Cross compilation [tutorial][3] for v0.12.x

Cross compilation [tutorial][5] for v0.14.x

[Chrome branding][6] (enable proprietary codecs)

### Older versions

For building older versions please check the [docs][2] directory.
Most probably each version will require extra tweaks in order to build successfully.

[1]: https://github.com/LeonardLaszlo/nw.js-armv7-binaries/releases
[2]: https://github.com/LeonardLaszlo/nw.js-armv7-binaries/tree/master/docs
[3]: http://forum.odroid.com/viewtopic.php?f=52&t=16072
[4]: http://docs.nwjs.io/en/latest/For%20Developers/Building%20NW.js
[5]: https://github.com/nwjs/nw.js/issues/1151#issuecomment-222101059
[6]: http://docs.nwjs.io/en/latest/For%20Developers/Enable%20Proprietary%20Codecs
