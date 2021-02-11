# Example InSpec Profile

This example shows the implementation of an InSpec profile with Effortless Audit using the multiple profile option by specifying `scaffold_profiles` in the `plan.sh` file.

## Multiple Profiles

To use multiple profiles in the audit run, the property `scaffold_profiles` must be set in the `plan.sh` file.  This should be an array which lists a name of directories to include.  This example will include `./profile1` and `./profile2` directories from the top level of the repository as Inspec profiles to be consumed during the run:

```sh
scaffold_profiles=(profile1 profile2)
```

## Single Profile

To run a single profile, the top level of the repository should be an Inspec directory with an `inspec.yml` file and a `controls` directory.  That structure is included in this repository as well but is not used.  To test how a single profile method works, comment out the `scaffold_profiles` line of the `plan.sh` file.
