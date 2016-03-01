# clicksend-php
A wrapper for our REST API - SMS, voice, post, email, fax.

##### API docs can be accessed [here](https://developers.clicksend.com/docs/):

#

##### You’ll need a free account to get [started](https://dashboard.clicksend.com/#/signup/step1/): 

#

How To Build: 
=============
The generated code uses a PHP library namely UniRest. The reference to this
library is already added as a composer dependency in the generated composer.json
file. Therefore, you will need internet access to resolve this dependency.

Installation:
===========

****For using this SDK do the following:****

	1. Go to sdk project root folder.
	2. Use composer to install the dependencies. If you don't have composer you can download it on https://getcomposer.org/download
	3. Enter command `composer update` to install dependencies.

Sample Code:
=============

***Send SMS***

```php
<?php

require_once 'vendor/autoload.php';

use ClickSendV3APILib\Controllers\SMSController;

$messages =  [
        [
            "source" => "php",
            "from" => "sendmobile",
            "body" => "Jelly liquorice marshmallow candy carrot cake 4Eyffjs1vL.",
            "to" => "+61411111111",
            "schedule" => 1536874701,
            "custom_string" => "this is a test"
        ],
        [
            "source" => "php",
            "from" => "sendlist",
            "body" => "Chocolate bar icing icing oat cake carrot cake jelly cotton MWEvciEPIr.",
            "list_id" => 428,
            "schedule" => "1436876011",
            "custom_string" => "This is a test"
        ]
];

try {
    $controller = new SMSController('your-username', 'your-api-key');
    $response = $controller->sendSms($messages);
    //response will return an object
    print_r($response);
} catch(APIException $e) {
    print_r($e->getResponseBody());
}

?>
```

