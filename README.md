#Sublime-Silex

This is a Sublime Text package with useful snippets for [Silex](http://silex.sensiolabs.org), the PHP micro-framework.

##How to install##

###With Package Control###

Run “Package Control: Install Package” command, find and install `Silex Snippets` plugin.
###Manually###

[Download](https://github.com/franciscosantamaria/sublime-silex/archive/master.zip) git repo into your packages folder.

You can also make a clone of the repository into your packages folder:

    git clone https://github.com/franciscosantamaria/sublime-silex.git silex-snippets

##Shortcuts##

###Routing###

`siget` GET route.

```php
$app->get('', function () use ($app) {

}
);

```

`sipost` POST route.

```php
$app->post('', function () use ($app) {

}
);

```

`siput` PUT route.

```php
$app->put('', function () use ($app) {

}
);

```

`simatch` Math all methods routes (GET, POST, PUT and DELETE).

```php
$app->match('', function () use ($app) {

}
);

```

`sidel` DELETE route.

```php
$app->delete('', function () use ($app) {

}
);

```

###Middlewares###

`siafter` After middleware. Allows tweak the Response before it is sent to the client.

```php
$app->after(function (Request $request, Response $response) {

}
);
```

`sibefore` Before middleware. Allows tweak the Request before the controller is executed.

```php
$app->before(function (Request $request) {

}
);
```

`sifinish` Finish middleware. Allows you execute tasks after the Response has been sent.

```php
$app->finish(function (Request $request, Response $response) {

}
);
```
###Providers###
####Registering service providers####
`sidoctrinere` Registers DoctrineServiceProvider.

```php
$app->register(new Silex\Provider\DoctrineServiceProvider(), array(
    'db.options' => array(
        'driver'   => '',
        'dbname'   => '',
        'host'     => '',
        'user'     => '',
        'password' => '',
    ),
));
```

`simonologre` Registers MonologServiceProvider.

```php
$app->register(new Silex\Provider\MonologServiceProvider(), array(
        'monolog.logfile' => '',
        'monolog.level' => '',
        'monolog.name' => '',
    )
);
```

`siserializerre` Registers SerializerServiceProvider.

```php
$app->register(new Silex\Provider\SerializerServiceProvider());
```

`sisessionre` Registers SessionServiceProvider.

```php
$app->register(new Silex\Provider\SessionServiceProvider());
```

`simailerre` Registers SwiftmailerServiceProvider.

```php
$app->register(new Silex\Provider\SwiftmailerServiceProvider(), array(
    'swiftmailer.options' => array(
            'host' => '',
            'port' => '',
            'username' => '',
            'password' => '',
            'encryption' => ,
            'auth_mode' => ,
    ),
));
```

`sitransre` Registers TranslationServiceProvider.

```php
$app->register(new Silex\Provider\TranslationServiceProvider(), array(
    'locale_fallbacks' => array('en'),
));
```

`sitwigre` Registers TwigServiceProvider.

```php
$app->register(new Silex\Provider\TwigServiceProvider(), array(
    'twig.path' => '',
));
```

`siurlgere` Registers UrlGeneratorServiceProvider.

```php
$app->register(new Silex\Provider\UrlGeneratorServiceProvider());
```

`sivalre` Registers ValidatorServiceProvider.

```php
$app->register(new Silex\Provider\ValidatorServiceProvider());
```

###Services###
####Monolog####
`simonodebug` Creates log entry with 'debug' level.

```php
$app['monolog']->addDebug('');
```

`simonoerr` Creates log entry with 'error' level.

```php
$app['monolog']->addError('');
```

`simonoinfo` Creates log entry with 'info' level.

```php
$app['monolog']->addInfo('');
```

`simonowarn` Creates log entry with 'warning' level.

```php
$app['monolog']->addWarning('');
```

####Serializer####
`siserialize`  Serializes data using an instance of Symfony\Component\Serializer\Serializer.

```php
$app['serializer']->serialize(,'');
```

`sideserialize` Deserializes data into the given type using an instance of Symfony\Component\Serializer\Serializer.

```php
$app['serializer']->deserialize(,'','');
```

####Session####
`siseget` Fetchs a value from session storage.

```php
$app['session']->get('');
```

`siseset` Stores a value in the session storage.

```php
$app['session']->set('',);
```

####Swiftmailer####
`simailsend` Sends a mail.

```php
$app['mailer']->send();
```

####Translation####
`sitrans`

```php
$app['translator']->trans($message,array(
    '' => '',
    ));
```

####Twig####
`sitwig` Renders a twig file.

```php
$app['twig']->render('',array(
    '' => '',
));
```

####UrlGenerator####
`siurlgen` Generates URL for named route.

```php
app['url_generator']->generate('',array('' => ''));
```

##Contribute##

If you have seen mistakes or want to add new snippets, feel free to fork the project and make any pull request you want.
