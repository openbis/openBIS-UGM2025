Title of the proposed topic for the hackathon sessions:

# openBIS - Storage Access - in a multi-group instance

Name of person proposing the topic:

## Kristian Ullrich and Carsten Fortmann-Grote

Organization Name:

## Max Planck Institute For Evolutionary Biology

Technologies used:

## Java, JavaScript

URL of public repositories of the project:

### https://sissource.ethz.ch/sispub/openbis

### Summary of the project:

In openBIS it is possible to define `Storages`. These `Storages` are either defined in the `General ELN Settings` or in the `Settings` for each defined `Group`.
These `Storages` are then bound to these parent `Spaces`.

There are two open topics that we are faced during our work with openBIS and want to address in this hackaton session.

To use any kind of `Storage` to mimick lab-work, one would need to:

1. be able to keep and create an `empty` `Storage`to be filled afterwards (at the moment only possible via the API)
2. manage `access` rights for that `Storage`
3. allow `access` behind the borders of the `active` group or `HomeSpace` (at the moment not possible, the `Storages` just can not be selected)
5. be able to select `global` `Storages` even from within a `UserSpace` or any other `active` shared `group` experiments

     this is important because there are many scenarios where a Researcher writes its own `Notebook` but would still use `OBJECTs` which are stored outside the corresponding `GroupSpace`

     this becomes even more important to technical stuff that are working for `core-facilities` to be able to share `OBJECTs` in `Storages` not linked to any `group`

This hackaton is an advanced topic to address `Storage Access` in a `multi-group instance` setup, but might high-impact due to its urgent need to correctly and efficiently deal with object storage and object sharing in real wet-lab scenarios.
