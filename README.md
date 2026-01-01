# PVAutonomy Inverter Registry (Test)

Community-driven register definitions for solar inverters.

## Supported Inverters

| Manufacturer | Series | Models |
|-------------|--------|--------|
| Growatt | SPH | SPH10K-TL3-BH-UP |

## Usage

Add to your ESPHome configuration:

```yaml
substitutions:
  sensor_prefix: "sph10k_haus_01"  # Format: {series}_{location}_{number}

packages:
  inverter:
    url: https://github.com/gshubi/esphome-registry-test
    file: esphome/inverters/growatt/sph/sph10k.yaml
    ref: main
```

## Requirements

- ESPHome 2022.1.0 or later
- VPP Mode enabled on Growatt inverter (via ShinePhone app)
- RS485 connection to inverter

## Included Sensors

### SPH10K Package (22 sensors + 1 control)

**PV Production:**
- PV1/PV2 Voltage, Current, Power

**Battery:**
- SOC, Voltage, Current, Power, Temperature

**Grid:**
- Power, Frequency, Voltage L1/L2/L3

**System:**
- Load Power, Inverter Status/Temperature
- PV Generation Today/Total

**APR Control:**
- Active Power Rate (5-100%)

## Structure

```
esphome/
└── inverters/
    └── growatt/
        └── sph/
            └── sph10k.yaml
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

MIT License - see [LICENSE](LICENSE)
