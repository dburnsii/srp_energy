# srp_energy

The `srp_energy` integration shows information from Srp hourly energy usage report for their customers. The srpenergy module fetches the data from the SRP data API.

You need a Username, Password, and AccountId which you can create at [Srp](https://www.srpnet.com).

## Installation

1. Using the tool of choice open the directory (folder) for your HA configuration (where you find `configuration.yaml`).
2. If you do not have a `custom_components` directory (folder) there, you need to create it.
3. In the `custom_components` directory (folder) create a new folder called `srp_energy`.
4. Download _all_ the files from the `custom_components/srp_energy/` directory (folder) in this repository.
5. Place the files you downloaded in the new directory (folder) you created.
6. Restart Home Assistant.
7. Move on to the configuration.

Using your HA configuration directory (folder) as a starting point you should now also have this:
```text
custom_components/srp_energy/__init__.py
custom_components/srp_energy/manifest.json
custom_components/srp_energy/sensor.py
```

## Example configuration.yaml

```yaml
sensor:
  - platform: srp_energy
    username: YOUR_USERNAME
    password: YOUR_PASSWORD
    id: YOUR_ACCOUNT_ID
```

### Configuration options

Key | Type | Required | Description
-- | -- | -- | --
`username` | `string` | `True` | Your username for SRP.
`password` | `string` | `True` | Your password for SRP.
`id` | `string` | `True` | Your account id for SRP (digits only).
`tou` | `boolean` | `False` | Whether your account uses a Time-Of-Use plan (EZ plans included)

## Contributions are welcome!

If you want to contribute to this please read the [Contribution guidelines](CONTRIBUTING.md)
