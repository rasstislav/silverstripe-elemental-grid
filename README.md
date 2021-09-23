# SilverStripe Elemental Grid

## Introduction

This module converts the elemental module (https://github.com/silverstripe/silverstripe-elemental) into a grid module.

![Overview](docs/images/screen01.png)

## Requirements

* SilverStripe CMS ^4.0
* dnadesign/silverstripe-elemental ^4
* Frontend css supporting a grid system (col-xs-X col-sm-X col-md-X col-lg-X visible-XS/SM/MD/LG hidden-XS/SM/MD/LG and col-xs-offset-X etc)

## Installation
```
composer require thewebmen/silverstripe-elemental-grid:^2.0
```

In the following example we create a new GridPage typo to use the Grid.\

**app/src/Model/GridPage.php**
```php
<?php
class GridPage extends Page
{
}
```
**app/_config/grid.yml**
```yaml
GridPage:
    extensions:
        - DNADesign\Elemental\Extensions\ElementalPageExtension
```

## Further configuration
For more information about configuration, check out the documentation in the `docs` directory.

* [Configuration](docs/configuration.md)

## PHPCS Fixer/PHPStan
PHPCSFixer and PHPStan are included to resolve codestyle fixes and do static analytic on the code.

You can run the following commands in your **project root directory**.

### PHP CodeStyle fixer
Dry-run to spot codestyle issues:\
`./vendor/bin/php-cs-fixer fix ./vendor/thewebmen/silverstripe-elemental-grid --diff --dry-run`\
Fix issues:\
`./vendor/bin/php-cs-fixer ./vendor/thewebmen/silverstripe-elemental-grid fix`

### PHPStan
`./vendor/bin/phpstan analyse -c ./vendor/thewebmen/silverstripe-elemental-grid/phpstan.neon ./vendor/thewebmen/silverstripe-elemental-grid`

# License
See [License](LICENSE)

## Maintainers
* [Webmen](https://www.webmen.nl/) <developement@webmen.nl>

## Development and contribution
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.\
See read our [contributing](CONTRIBUTING.md) document for more information.
