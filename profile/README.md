# Embedded Systems for IoT · Group E

Firmware projects from **Group E** for *Embedded Platforms and Communications for IoT*, a course in the
[Master in Internet of Things (MIoT)](https://www.etsist.upm.es/estudios-ingenieria-sistemas-telecomunicaciones-madrid/masters-ingenieria-madrid/Master-IoT)
at Universidad Politécnica de Madrid.

Every project runs on real hardware and is documented so that it can be rebuilt from scratch:
the wiring, how to build and flash it, the architecture, and how it was tested.

## Projects

| Project | What it does | Highlights |
|---|---|---|
| [brightness_control](https://github.com/master-iot-embedded-group-e/brightness_control) | Measures ambient light with an LDR and shows the level on an RGB LED. A button switches between three operating modes. | Zephyr threads and message queues, a Mealy FSM, debounced short and long button presses, and ADC runtime power management. The same code drives both common-anode and common-cathode LEDs through devicetree overlays. |

## Stack

- **RTOS:** [Zephyr](https://zephyrproject.org/)
- **Hardware:** STMicroelectronics NUCLEO-WL55JC (STM32WL55, Cortex-M4)
- **Toolchain:** `west`, CMake, OpenOCD
- **Workflow:** Gitflow, with every change merged into `develop` through a pull request. Commits follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).

## Team

| | |
|---|---|
| Carlos Egea | [@cegea](https://github.com/cegea) |
| Omar Piñeiro | [@Omarpparada](https://github.com/Omarpparada) |
