#Sublime-Silex

This is a Sublime Text package with useful snippets for Silex, the PHP micro-framework.

##How to install##

###With Package Control###

Run “Package Control: Install Package” command, find and install `Silex Snippets` plugin.
###Manually###

[Download](https://github.com/franciscosantamaria/sublime-silex/archive/master.zip) git repo into your packages folder.

You can also make a clone of the repository into your packages folder:

    git clone https://github.com/franciscosantamaria/sublime-silex.git silex-snippets

##Shortcuts##

###Routing###

`siget`

```php
$app->get('', function () use ($app) {

}
);

```

`sipost`

```php
$app->post('', function () use ($app) {

}
);

```

`siput`

```php
$app->put('', function () use ($app) {

}
);

```

`simatch`

```php
$app->match('', function () use ($app) {

}
);

```

`sidel`

```php
$app->delete('', function () use ($app) {

}
);

```

###Middlewares###

`siafter`

```php
$app->after(function (Request $request, Response $response) {

}
);
```

`sibefore`

```php
$app->before(function (Request $request) {

}
);
```

`sifinish`

```php
$app->finish(function (Request $request, Response $response) {

}
);
```
###Providers###
####Registering service providers####
`sidoctrinere`

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

`simonologre`

```php
$app->register(new Silex\Provider\MonologServiceProvider(), array(
    'db.options' => array(
        'monolog.logfile' => '',
        'monolog.level' => '',
        'monolog.name' => '',
    ),
));
```

`sitwigre`

```php
$app->register(new Silex\Provider\TwigServiceProvider(), array(
    'twig.path' => '',
));
```

###Services###
####Monolog####
`simonodebug`

```php
$app['monolog']->addDebug('');
```

`simonoerr`

```php
$app['monolog']->addError('');
```

`simonoinfo`

```php
$app['monolog']->addInfo('');
```

`simonowarn`

```php
$app['monolog']->addWarning('');
```

####Twig####
`sitwig`

```php
$app['twig']->render('',array(
    '' => '',
));
```
##Contribute##

If you have seen mistakes or want to add new snippets, feel free to fork the project and make any pull request you want.