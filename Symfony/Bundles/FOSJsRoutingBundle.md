# FOSJsRoutingBundle

This bundle allows to expose Symfony Routes to JavaScript, so you can generate
relative or absolute URLs in the browser using the same routes as in the backend.

[Documentation](https://symfony.com/doc/master/bundles/FOSJsRoutingBundle/index.html)

### Installation

```bash
    composer require friendsofsymfony/jsrouting-bundle
```

```php
    # app/AppKernel.php
    $bundles = array(
        # ...
        new FOS\JsRoutingBundle\FOSJsRoutingBundle(),
        # ...
    );
```

```yaml
    # app/config/routing.yml
    fos_js_routing:
        resource: "@FOSJsRoutingBundle/Resources/config/routing/routing.xml"
```

```bash
    app/console assets:install --symlink web
```
