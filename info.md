# srp_energy


The `srp_energy` integration shows information from Srp hourly energy usage report for their customers. The srpenergy module fetches the data from the SRP data API.

You need a Username, Password, and AccountId which you can create at [Srp](https://www.srpnet.com).

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

