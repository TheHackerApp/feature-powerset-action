# feature-powerset-action

A composite action for generating a powerset of features for a Rust crate. This is intended to be
used as the precursor to one or more [matrix builds][matrix-builds].

The action parses the `Cargo.toml` file and extracts the features from the `[features]` table.
After which, the powerset is generated and output as a JSON array that can be used by other
jobs or steps.

## Inputs

All inputs are optional.

| Name | Description | Default |
| ---- | ----------- | ------- |
| `manifest` | The path to the `Cargo.toml` file. | `Cargo.toml` |

## Outputs

| Name | Description |
| ---- | ----------- |
| `features` | The powerset of features as a JSON array. |

[matrix-builds]: https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions#jobsjob_idstrategymatrix
