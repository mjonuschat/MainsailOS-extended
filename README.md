<!-- Improved compatibility of back to top link: See: https://github.com/mjonuschat/MainsailOS-extended/pull/73 -->
<a name="readme-top"></a>

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

<!-- ABOUT THE PROJECT -->
# MainsailOS (extended)

## About The Project

This project takes the fantastic MainsailOS distribution for 3D Printers and adds the (few) features I desired for a polished out-of-the-box experience, namely a bootsplash that hides the diagnostic Linux boot messages and KlipperScreen to replace the default LCD interface.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Getting Started

This repository contains a [CustomPiOS](https://github.com/guysoft/CustomPiOS) distribution that takes the latest official MainsailOS image and extends it by adding the following features:

- Boot splash screen
- KlipperScreen
- Localization settings

### Customizing the bootsplash screen

#### Choosing the default Voron bootsplash color

Add (or modify) the following line in your `config.local` file to choose the
desired color scheme:

```bash
export BOOTSPLASH_IMAGE="voron/voron_splash_red.png"
```

This will activate the desired image as the bootsplash screen.

#### Custom image as a splash screen

Copy the desired image into the
`src/modules/bootsplash/filesystem/root/usr/share/bootscreens/custom` path. Make
sure it is a **PNG** image with a width of **1024** and a height of **600**
pixels. If your screen has a different aspect ratio it might be OK to deviate. 

Activate the custom image by adding the following code to your `config.local` file.
```bash
export BOOTSPLASH_IMAGE="custom/my-custom-bootsplash.png"
```

### Building the image

The build process for this image utilizes **Docker** and needs `docker-compose` to run.
Start the build by running the following command in the root directory of the project:

```bash
./build
```

If the build process succeeded you should find a new compressed MainsailOS image
in the `src/workspace/` folder with a name similar to
`MainsailOS-buster-lite-0.7.1-extended.zip`.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- INSTALLING -->
## How to install MainsailOS-extended

You can find detailed instructions in the MainsailOS [documentation](https://docs.mainsail.xyz/setup/mainsail-os).

Installation via [Raspberry Pi Imager](https://docs.mainsail.xyz/setup/mainsailos/pi-imager) [Etcher](https://github.com/balena-io/etcher) is highly recommended.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated** but please check if the contribution would benefit a larger audience and submit it to the Mainsail or MainsailOS repositories if that is the case.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->
## License

Distributed under the GPLv3 License. See `LICENSE` for more information.

The Voron-themed bootsplash images have been created and shared by samwiseg0
under the [GPLv3
License](https://github.com/samwiseg0/misc_3dprinting/blob/main/LICENSE) in the
[samwiseg0/misc_3dprinting](https://github.com/samwiseg0/misc_3dprinting/tree/main/guides/voron_rpi_bootscreen/Images)
repository.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- SUPPORT -->
## Support

If you're having any problems, please [raise an issue][issues-new] on GitHub, and I will do my best to help.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

This project is standing on the shoulders of giants and without their work, none
of this would have been possible.

* [Mainsail](https://docs.mainsail.xyz)
* [KlipperScreen](https://klipperscreen.readthedocs.io/en/latest/)
* [CustomPiOS](https://github.com/guysoft/CustomPiOS)
* [Voron Design](https://vorondesign.com)
* [samwiseg0](https://github.com/samwiseg0/misc_3dprinting/tree/main/guides/voron_rpi_bootscreen/Images)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
[contributors-shield]: https://img.shields.io/github/contributors/mjonuschat/MainsailOS-extended.svg?style=for-the-badge
[contributors-url]: https://github.com/mjonuschat/MainsailOS-extended/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/mjonuschat/MainsailOS-extended.svg?style=for-the-badge
[forks-url]: https://github.com/mjonuschat/MainsailOS-extended/network/members
[stars-shield]: https://img.shields.io/github/stars/mjonuschat/MainsailOS-extended.svg?style=for-the-badge
[stars-url]: https://github.com/mjonuschat/MainsailOS-extended/stargazers
[issues-shield]: https://img.shields.io/github/issues/mjonuschat/MainsailOS-extended.svg?style=for-the-badge
[issues-url]: https://github.com/mjonuschat/MainsailOS-extended/issues
[issues-new]: https://github.com/mjonuschat/MainsailOS-extended/issues
[license-shield]: https://img.shields.io/github/license/mjonuschat/MainsailOS-extended.svg?style=for-the-badge
[license-url]: https://github.com/mjonuschat/MainsailOS-extended/blob/master/LICENSE
