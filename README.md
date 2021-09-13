# PHP HTTP Method Manager

Perform actions from the HTTP method used by means of PHP

## Installation

Use Composer to install the image with this command:

`composer require sikessem/http-method`

## Usage

Example code:

```php
<?php

use SIKessEm\SIKessEm\{
  function method
};

require_once $COMPOSER_AUTOLOAD_FILE; // Replace $COMPOSER_AUTOLOAD_FILE by the path of your vendor autoload

$method = method($_SERVER['REQUEST_METHOD']);
$method->in(['post', 'get'], function (string $verb) {
  //... Do this for all GET or POST methods
}); 
$method->notIn(['put', 'delete'], function (string $verb) {
  //... Do this for all methods except HEAD and OPTIONS
});
$method->is('head', function (string $verb) {
  //... Do this for all HEAD methods
});
$method->isNot('options', function (string $verb) {
  //... Do this for all methods except OPTIONS
});
$method->do(function (string $verb) {
  //... Do this for all types of methods
});
```

## Author

SIGUI Kessé Emmanuel ([https://sikessem.com/](https://sikessem.com/)) <[opensource@sikessem.com](mailto:opensource@sikessem.com)> | [GitLab](https://gitlab.com/SIKessEm) | [GitHub](https://github.com/SIKessEm) | [npm](https://npmjs.org/~sikessem) | [Composer - Packagist](https://packagist.org/packages/sikessem/) | [Twitter](https://twitter.com/SIKessEm_tweets)


## Security Reports

Please send any sensitive issue to [report@sikessem.com](mailto:report@sikessem.com). Thanks!