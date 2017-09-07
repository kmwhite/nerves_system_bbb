# ODROID-XU4 Base System for Nerves

[![CircleCI](https://circleci.com/gh/kmwhite/nerves_system_xu4.svg?style=svg)](https://circleci.com/gh/kmwhite/nerves_system_xu4)

This is the base Nerves System configuration for the [ODROID-XU4](http://www.hardkernel.com/main/products/prdt_info.php?g_code=G143452239825), but it may also work on the [ODROID-HC1](http://www.hardkernel.com/main/products/prdt_info.php?g_code=G150229074080) and [ODROID-XU3](http://www.hardkernel.com/main/products/prdt_info.php?g_code=G140448267127), but I lack the hardware to test. Your milage may vary.

![BeagleBone Black image](assets/images/beaglebone-black.png)
<br><sup>[Image credit](#fritzing)</sup>

| Feature              | Description                     |
| -------------------- | ------------------------------- |
| CPU                  | Samsung Exynos5422 Cortex™-A15 2.0Ghz quad core and Cortex™-A7 quad core CPUs |
| Video                | Mali-T628 MP6(OpenGL ES 3.0/2.0/1.1 and OpenCL 1.1 Full profile) |
| Memory               | 2Gbyte LPDDR3 RAM at 933MHz (14.9GB/s memory bandwidth) PoP stacked |
| Storage              | Up to 64GB of space via eMMC5.0 HS400 Flash Storage |
| Linux kernel         | 4.7.4 |
| IEx terminal         | TBD |
| GPIO, I2C, SPI       | TBD |
| ADC                  | TBD |
| PWM                  | TBD |
| UART                 | TBD; Need to purchase USB-UART cable to test |
| Camera               | TBD |
| Ethernet             | Yes |
| WiFi                 | Other, requires USB WiFi dongle/driver. Upon succuessful image build, I'll include the drivers for the ones on HardKernel |

## Preparing your XU4


## Console access


## Linux versions


## Device tree overlays


### Universal I/O


### ADCs


### SPI


## Supported USB WiFi devices


## Other Variants (ODROID-XU3, ODROID-HC1, etc)

Be aware that this Nerves system is not tested on those. If you would like to try it on your device, PLEASE let me know your results so I can include them here!

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed as:

  1. Add nerves_system_bbb to your list of dependencies in `mix.exs`:

        def deps do
          [{:nerves_system_xu4, "~> 0.12.0"}]
        end

  2. Ensure nerves_system_xu4 is started before your application:

        def application do
          [applications: [:nerves_system_xu4]]
        end
