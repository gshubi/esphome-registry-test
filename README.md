# ESPHome Registry Test

Test repository for ESPHome `github://` package includes.

## Usage

```yaml
substitutions:
  sensor_prefix: "sph10k_haus_01"

packages:
  registers: !include
    file: github://gshubi/esphome-registry-test/esphome/inverters/growatt/sph/sph10k.yaml@main
```

## Structure

```
esphome/
└── inverters/
    └── growatt/
        └── sph/
            └── sph10k.yaml
```
