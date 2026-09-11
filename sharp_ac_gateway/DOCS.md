# Configuration and operation

Options and defaults are listed in [config.yaml](config.yaml). Configure device
endpoints in the installed App's options.

`control_enabled` defaults to `true`. Set it to `false` before starting a new
installation or migration to allow read-only enrollment and polling.

Provide MQTT through Home Assistant Supervisor and configure access to the
private container registry. Keep protection mode enabled and ECO correlation
capture off during normal use.

Use Home Assistant's App update controls for published versions.

## Migration from a Local App

The repository App has a different internal identifier. Prepare and verify a
transfer of the complete App data before uninstalling the existing App or
starting its replacement. A backup alone does not perform that transfer.

Run only one Gateway for the same devices. Preserve device identities, command
history, and the existing HomeKit bridge pairing.
