# dora-openarm-quitter

A [Dora](https://dora-rs.ai/) node that exits when it receives a `quit` command.

## Usage

This node listens to all Dora `INPUT` events.

### Inputs

| Input ID | Type | Description |
| --- | --- | --- |
| `command` | Arrow array where first value is a string | If the first value is `"quit"`, the node exits. Any other `command` value is ignored. |
| any other input ID | Any Arrow value | The input is forwarded to an output with the same ID and metadata. |

### Outputs

| Output ID | Type | Description |
| --- | --- | --- |
| same as input ID (except `command`) | Same as input value | For each non-`command` input, the node sends an output with the same ID, value, and metadata. |

## License

Licensed under the Apache License 2.0. See [LICENSE](LICENSE) for details.

Copyright 2026 Enactic, Inc.

## Code of Conduct

All participation in the OpenArm project is governed by our [Code of Conduct](CODE_OF_CONDUCT.md).
