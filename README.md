# RD Station Integration to Zend Framework 2/3

### Install ###

Run 
```
$php composer.phar vinimarcili/vrm-rd-station-integration-to-zf
```

or on your Zend Project

```
$php composer require vinimarcili/vrm-rd-station-integration-to-zf
```

### Usage ###

```PHP
<?php

// Use Module
use VRMRdStationIntegration\RDStation\RDStation;

// Mount your data array, the field email ir required
$array = array(
    'email' => 'lead@email.com',
    'name'  => 'Bob'
);

// Pass the array
$rdstation = new RDStation($array);

// Public token RD Station
$rdstation->token = 'token';

// Form identifier
$rdstation->identifier = 'identifier';

// Exclude fields
$rdstation->ignore_fields(array('field1', 'field2', 'field3'));

// Redirect with 'ok' status
$rdstation->redirect_success = 'http://linkhere.com';

// Redirect with 'error' status
$rdstation->redirect_error = 'http://linkhere.com';

// Creating leads
$rdstation->createLead();

?>
```
