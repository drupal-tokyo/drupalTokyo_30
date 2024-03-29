[![](https://www.drupal.org/files/styles/grid-3/public/project-images/Medium-Logo%20Color%20with%20padding.png)](http://www.drupal.org/project/varbase)

[![Build Status](https://travis-ci.org/Vardot/varbase.svg?branch=8.x-6.4)](https://travis-ci.org/Vardot/varbase/builds/485040548) Varbase 8.6.4

# Varbase Project

Project template for [Varbase distribution](http://www.drupal.org/project/varbase).


## Create a Varbase project with [Composer](https://getcomposer.org/download/):

To install the most recent stable release of Varbase 8.6.x run this command:
```
composer create-project Vardot/varbase-project:^8.6.4 PROJECT_DIR_NAME --no-dev --no-interaction
```

To install the dev version of Varbase 8.6.x run this command:
```
composer create-project vardot/varbase-project:8.6.x-dev PROJECT_DIR_NAME --stability dev --no-interaction
```

## [Create a new Vartheme sub theme for a project](https://github.com/Vardot/varbase/tree/8.x-6.x/scripts/README.md)

## [Automated Functional Testing](https://github.com/Vardot/varbase/blob/8.x-6.x/tests/README.md)

## [Varbase Gherkin features](https://github.com/Vardot/varbase/blob/8.x-6.x/tests/features/varbase/README.md)

## [Varbase 8.6.x Developer Guide](https://docs.varbase.vardot.com)

## [CHANGELOG for Varbase](https://github.com/Vardot/varbase/blob/8.x-6.x/CHANGELOG.md)

## [General instructions on how to update Varbase](https://github.com/Vardot/varbase/blob/8.x-6.x/UPDATE.md)




# Notices

### Requiring Drupal Modules with Dev Version in varbase-project/composer.json
You will notice that we're requiring some Drupal modules in dev state with its commit hash. This is because of a bug in Composer. And it was discussed in https://github.com/composer/composer/issues/6366 and is highlighted in Composer documentation as follows:

> Note: This feature has severe technical limitations, as the composer.json metadata will still be read from the branch name you specify before the hash. You should therefore only use this as a temporary solution during development to remediate transient issues, until you can switch to tagged releases. The Composer team does not actively support this feature and will not accept bug reports related to it.

Therefore, our workaround, is to explicitly tag the commit hash we want in `varbase-project/composer.json`. This means that ALL Drupal modules dependencies which are in dev stage, are duplicated as a requirement for composer in both `varbase-project/composer.json` and `varbase/composer.json`.

This workaround will remain, until either a module has a tag (that we can tag without the commit hash) or a fix is provided from composer - hopefully in the near future!

Read more at: https://www.drupal.org/node/2903606#comment-12230769
