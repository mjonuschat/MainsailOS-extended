# bootsplash

CustomPiOS module to enable the bootsplash screen on startup.

**WARNING**: This module by default disables the V3D driver as starting the driver interferes with the output of the splash screen. None of the default Klipper functionality depends on 3D accelerated GPU output given that it's headless so this should
not be a problem.

If you want to re-enable the driver set the following in your `config.local`, but the bootsplash screen will only be visible for a second or two.

```bash
export BOOTSPLASH_DISABLE_V3D="no"
```

## Customizing the bootsplash screen

### Choosing the default Voron bootsplash color

Add (or modify) the following line in your `config.local` file to choose the
desired color scheme:

```bash
export BOOTSPLASH_IMAGE="voron/voron_splash_red.png"
```

This will activate the desired image as the bootsplash screen.

### Custom image as a splash screen

Copy the desired image into the
`src/modules/bootsplash/filesystem/root/usr/share/bootscreens/custom` path. Make
sure it is a **PNG** image with a width of **1024** and a height of **600**
pixels. If your screen has a different aspect ratio it might be OK to deviate. 

```bash
export BOOTSPLASH_IMAGE="custom/my-custom-bootsplash.png"
```
