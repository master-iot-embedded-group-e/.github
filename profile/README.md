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
| [drone_telemetry](https://github.com/master-iot-embedded-group-e/drone_telemetry) *(in progress)* | Final project of the course: a tracking and telemetry node for a drone. It reports position, motion, ambient light, temperature and humidity, and classifies the drone as idle, flying or in trouble. It monitors the drone but does not control it. | GPS over UART, an MPU6050 IMU and an Si7021 sensor on a shared I2C bus, an LDR on the ADC, and an RGB status LED. Four operating modes selected with a button. In simulator mode it streams fixed-width telemetry frames at 10 Hz, with a checksum, to a flight simulator on the PC. |

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
