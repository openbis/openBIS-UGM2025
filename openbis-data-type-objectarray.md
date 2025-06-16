Title of the proposed topic for the hackathon sessions:

# Create respectively extend the `DataType` `OBJECT` to an `OBJECTARRAY`.

Name of person proposing the topic:

## Kristian Ullrich and Carsten Fortmann-Grote

Organization Name:

## Max Planck Institute For Evolutionary Biology

Technologies used:

## Java, JavaScript

URL of public repositories of the project:

### https://sissource.ethz.ch/sispub/openbis

### Summary of the project:

In openBIS it is possible to add to any `OBJECT` (here referred to as `TARGET`) a new `Property` of `DataType=OBJECT` defining e.g. an `ObjectType=BACTERIA`,
meaning one can link beside `Parent` and `Children` to the `TARGET` object another `OBJECT` (e.g. `BACTERIA001`).

This feature is already very good, since one can search quickly among the defined `ObjectType=BACTERIA` to select e.g. a `BACTERIA001` to be linked to the `TARGET`.

Anyhow, in our setup, to be able to assign multiple linked objects of the same `ObjectType`,
one would need to define as many input fields for the `TARGET` in the `openbis-ng-ui` as the number of objects, that one would like to link.

This would look like:
```
Code=LINKED_BACTERIA001; DataType=OBJECT; ObjectType=BACTERIA
Code=LINKED_BACTERIA002; DataType=OBJECT; ObjectType=BACTERIA
Code=LINKED_BACTERIA003; DataType=OBJECT; ObjectType=BACTERIA
and so on
```

To make this more efficient and more flexible we propose to add a new `Property` `DataType` named `OBJECTARRAY`.

The `DataType=OBJECTARRAY` should:

- allow multiple objects of the same `ObjectType` to be added to that `Property`
- search and select directly multiple objects of the same `ObjectType` (regular expression)
- automatically warn or reduce to a `SET` if one object is already present (de-duplication)

    to be discussed if duplicated values should be possible or not

This `new` feature might help the community to cover the explained scenario not relying on `Parent` and `Children` which can take multiple entries,
but have their own caveats (e.g. it is not allowed that `Parent` and `Children` are the same objcets, which makes sense in a hierachical thinking but not dealing with e.g. self-reproducing organisms).
