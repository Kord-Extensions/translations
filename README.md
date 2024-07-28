# Translations

This repository contains translations for Kord Extensions and its various first-party modules.
We keep each set of translations in a separate folder, which Gradle adds to the build for the respective module.

If you'd like to contribute to our translations, 
please [check out our Weblate project](https://hosted.weblate.org/engage/kord-extensions/).

[![Translation status](https://hosted.weblate.org/widget/kord-extensions/open-graph.png)](https://hosted.weblate.org/engage/kord-extensions/)

# Maintaining

When working on this repository, take note of the following:

- Each folder must match the bundle name. For example, the `pluralkit` folder contains files with names starting with 
  `pluralkit`.
- Each folder must contain a base translations file that contains every translation key and provides English 
  translations.
  For example, the `pluralkit` folder contains a `pluralkit.properties` file.

# Usage

When working with [Kord Extensions](https://github.com/kord-extensions/kord-extensions) itself, take note of the 
following:

- You must call `getTranslations()` in the build script for each module with translations.
  This will retrieve the translations from this repository that match the project name (the name of the folder
  containing the module) – for example, the translations for the  `func-mappings` module are stored here in the 
  `func-mappings` folder.
- You must prefix all bundles with `kordex.` in the code. For example, `pluralkit` becomes `kordex.pluralkit`.
