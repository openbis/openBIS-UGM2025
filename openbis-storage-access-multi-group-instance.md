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

We propose to support the following usage and management scenarios required in cases where storages are shared among multiple groups:

1. be able to keep and create an /empty/ `Storage`to be filled afterwards (at the moment only possible via the API)
1. manage `access` rights for that `Storage` so that individual users or groups can access any storage, in particular:
1. allow `access` beyond the limits of the `active` group or `HomeSpace` (at the moment not possible, the `Storages` cannot be selected)
1. be able to select `global` `Storages` even from within a `UserSpace` or any other `active` shared `group` experiments

These features are required in situations where e.g. a researcher writes her own `Notebook` but would still use `OBJECTs` which are stored outside the corresponding `GroupSpace`.
A prominent scenario is when core facility staff (e.g. sequence lab personal) needs shared access to a groups storage where the samples to be processed in the core facility are stored or where that same
core facility staff needs to share processed samples stored in the core facilities storage with individual members from other groups.

This proposal is an advanced topic to address `Storage Access` in a `multi-group instance` setup, but might have high-impact due to its urgent need to correctly and efficiently deal with object storage and object sharing in real wet-lab scenarios.
