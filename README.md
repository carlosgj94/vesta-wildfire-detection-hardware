# Vesta Fire Detector

Vesta is an early-stage project to build an open source hardware device for
wildfire detection. The hardware design is being done in KiCad, with the goal
of making a device that is easy to manufacture, cheap to deploy, and reliable
in harsh outdoor environments.

The device is intended to detect local environmental changes that may indicate
wildfire risk or an active fire, then report them as early as possible.

## Current Hardware

The current KiCad schematic includes:

- `STM32WL55CCU6`: main low-power microcontroller and wireless reporting
  platform.
- `BQ24074RGTR`: lithium battery charger and power-path management IC.
- `TPS63900DSKR`: efficient buck-boost regulator for the system supply.
- Solar panel inputs and battery connector for field power.
- Crystals, TVS protection, test points, jumpers, and passive support circuitry.

The current sensor set is:

- `BME688`: environmental sensor used for temperature, humidity, pressure, and
  gas/air-quality signals that can help identify smoke or fire-related changes.
- `SHT40-AD1F-R2`: temperature and humidity sensor used for accurate local
  climate readings and cross-checking the environmental baseline.

## Status

The project is still early stage. Full schematics should be ready soon, then the
work will move to PCB layout and 3D CAD. Embedded OS software will be provided
last, once the hardware platform is stable.
