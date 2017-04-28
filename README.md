# Cyphon Configurations

This is a depot for sharing [Cyphon](https://github.com/dunbarcyber/cyphon) configurations.

Configurations are saved as Django fixtures, which are described [here](https://docs.djangoproject.com/en/1.11/howto/initial-data/). If you'd like to share your Cyphon configurations with the community, please submit a pull request to this repo.

## Importing and Exporting Configurations

You can import and export configurations as fixtures by following the instructions [here](http://cyphon.readthedocs.io/en/latest/dev-guide/using-fixtures.html).

## Guidelines

When submitting fixtures, please avoid using primary keys (e.g., `"pk": 1`). An object with a primary key may throw an `IntegrityError` if an object with that same primary key already exists in a database. Instead, use [natural keys](https://docs.djangoproject.com/en/1.11/topics/serialization/#natural-keys). The exception to this rule is if an object is referenced by a [generic relation](https://docs.djangoproject.com/en/1.11/ref/contrib/contenttypes/#generic-relations), which currently does not support use of natural keys (see [ticket #23268](https://code.djangoproject.com/ticket/23268)).
