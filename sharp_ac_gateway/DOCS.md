# Configuration and operation

The supported option names, defaults, and validation rules are in
[config.yaml](config.yaml). Configure device endpoints only in the installed
App's options. Do not publish device addresses, credentials, backups, or
runtime state in issues or repository files.

The current package default for `control_enabled` is `true`. Setting it to
`false` allows read-only enrollment and polling, without command subscriptions
or a physical-write provider. Enabling control does not itself send a command.
For a new installation or migration, set control to `false` before starting.

MQTT must be available through Home Assistant Supervisor. Keep protection mode
enabled. Leave ECO correlation capture off during normal use.

Run only one Gateway for the same devices. App data contains persistent device
identity and command history; deleting or replacing it can change entities or
lose unresolved command state. Preserve the complete data when migrating.
Keep the existing HomeKit bridge pairing.

Use Home Assistant's App update controls for published catalog versions.
Moving from a Local App changes the internal Supervisor App identifier and
requires a verified data migration. Do not uninstall the existing App or start
a replacement until that migration is prepared. An App backup alone is not a
documented cross-identifier migration procedure.
