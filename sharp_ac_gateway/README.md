# Sharp AC Gateway

Connect compatible Sharp air conditioners to Home Assistant using a local
network connection and MQTT device discovery. Available controls depend on
the capabilities confirmed for each enrolled device.

The App obtains MQTT service settings from Home Assistant Supervisor. Command
state changes require confirmed device readback. A command whose outcome is
uncertain is not blindly retried.

Read the [configuration guide](DOCS.md) before installation. Private container
registry access is required. Existing Local App installations need a verified
migration before switching to this catalog.
