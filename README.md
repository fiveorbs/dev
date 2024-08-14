# VacantPlanet Development Settings and Tools

## Installation 

    composer require vacantplanet/development

## Usage

### Documentation snippets test runner

    ./vendor/bin/docs-test-runner path/to/docs/snippets

### php-cs-fixer

Add the following to your `.php-cs-fixer.dist.php`:

```php
<?php

declare(strict_types=1);

$finder = PhpCsFixer\Finder::create()->in([__DIR__ . '/src', __DIR__ . '/tests']);
$config = new VacantPlanet\Development\PhpCsFixer\Config();

return $config->setFinder($finder);
```
