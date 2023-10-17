# Yarnberry Unsupported Protocols Integration Test

This branch uses dependencies with the Git, GitHub and Exec protocols, which Cachi2
does not support. Executing `yarn install` in the presence of such dependencies would
lead to arbitrary code execution.

See:

```shell
git grep 'commit='
git grep 'exec:'
```

When processing this branch, Cachi2 should log the locator for each unsupported
dependency and raise an UnsupportedFeature error.
