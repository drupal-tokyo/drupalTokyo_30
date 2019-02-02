## テーマ

ディストリビューションを読んでベストプラクティスを見つけよう。

## 対象のディストリビューション:varbase

比較サンプル Lightning

- [Varbase: The Ultimate Drupal 8 CMS Starter Kit (Bootstrap Ready) | Drupal.org](https://www.drupal.org/project/varbase)

## composer project

- [Vardot/varbase-project: Project template for Varbase distribution](https://github.com/Vardot/varbase-project)
- [acquia/lightning-project: A Composer-based installer for the Lightning distribution of Drupal 8.](https://github.com/acquia/lightning-project)

## composer.json

多重構造になっている

- [varbase/composer.json at 8.x-6.x · Vardot/varbase](https://github.com/Vardot/varbase/blob/8.x-6.x/composer.json#L31)
  - [varbase_core/composer.json at 8.x-6.x · Vardot/varbase_core](https://github.com/Vardot/varbase_core/blob/8.x-6.x/composer.json)
- [lightning/composer.json at 8.x-3.x · acquia/lightning](https://github.com/acquia/lightning/blob/8.x-3.x/composer.json#L14)
  - [lightning_core - For more information about this repository, visit the project page at https://drupal.org/project/lightning_core](https://cgit.drupalcode.org/lightning_core/tree/composer.json)

### 共通

`oomphinc/composer-installers-extender`

[oomphinc/composer-installers-extender: Extend the composer/installers plugin to accept any arbitrary package type.](https://github.com/oomphinc/composer-installers-extender)

