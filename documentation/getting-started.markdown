# Getting started

## Download the bundle
Start by requiring the bundle with Composer:

```bash
composer require codedmonkey/semantic-ui-bundle "^2.0"
```

Composer will install the bundle into your `vendor` directory and adds the
dependency to your `composer.json` file.

If you're using Symfony Flex (required by default by Symfony 4 and up), that's
it! The bundle will automatically be registered in your application configuration.

## Enable the bundle (Symfony 3 only)
Enable the bundle by registering it in your `AppKernel` class:

```php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = [
        // ...
        new \CodedMonkey\SemanticUiBundle\SemanticUiBundle(),
    ];
}
```

## Next steps
* [How to render Semantic UI forms](forms.markdown)
* [How to render Semantic UI menus](knp-menu-bundle.markdown)
