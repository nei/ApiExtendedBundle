## API Extended Bundle

This bundle extend the core Akeneo API to add missing functionalities.

### Features:

- Add support for Product Model Delete via API.


Installing the bundle
---------------------
From your application root:

    $ php composer.phar require --prefer-dist "nei/api-extended-bundle=dev-master"

Register the bundle by adding the following line inside the `app/AppKernel.php` file, just before the "return $bundles;" line:

    $bundles[] = new Nei\Bundle\ApiExtendedBundle\NeiApiExtendedBundle();

Include the routing on the top of your main routing.yml file:

nei_api_extended:
    resource: "@NeiApiExtenedBundle/Resources/config/routing.yml"
    prefix:   /
