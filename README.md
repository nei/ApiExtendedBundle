## API Extended Bundle

This bundle extend the core Akeneo API to add missing functionalities.

### Features:

- Add support for Product Model Delete via API.


Installing the bundle
---------------------
From your application root:

    $ php composer.phar require --prefer-dist "nei/api-extended-bundle=dev-master"

Enable the bundle in the `app/AppKernel.php` file in the `registerProjectBundles()` method:

```php
    $bundles = [
        // ...
        new Nei\Bundle\ApiExtendedBundle\NeiApiExtendedBundle(),
    ]
```

Include the routing on the top of your main routing.yml file:

nei_api_extended:
    resource: "@NeiApiExtenedBundle/Resources/config/routing.yml"
    prefix:   /

Now let's clean your cache and dump your assets:

```bash
    php bin/console cache:warmup --env=prod
    php bin/console pim:installer:assets --env=prod
```