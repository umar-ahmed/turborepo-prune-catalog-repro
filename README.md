# turborepo-prune-catalog-repro
Minimal reproduction of issue with catalog: protocol plugin in Yarn 4 with Turborepo prune command

# Steps to reproduce

1. Clone the repository
2. Run `yarn install` to install dependencies
3. Run `yarn turbo prune a` to generate the pruned package in `out` directory

# Expected behavior

The `out` directory should contain the pruned package with the correct dependencies.

# Actual behavior

Error occurs during the pruning process indicating that it is unable to find a locator for `commander@catalog`.

```
turbo 2.5.5

Generating pruned monorepo for a in /workspaces/turborepo-prune-catalog-repro/out
 - Added a
  × Unable to find any locator for commander@catalog:
```