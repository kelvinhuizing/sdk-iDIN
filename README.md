# Paynl PHP SDK-iDIN

---

- [About](#about)
- [Installation](#installation) 
- [Installation without composer](#installation-without-composer) 
- [Setting up](#setting-up)
	- [1. The autoloader](#step-1-the-autoloader)  
	- [2. Your API token](#step-2-your-apitoken)
- [Examples](#examples)


---

### About
In order to use this SDK, you'll need to have an iDin account at Pay.nl

The iDin will be able to manage sub-merchants, and manage most of the task via the api that normally a merchant would do by logging in in the pay.nl admin.

Also this SDK extends the standard [Pay.nl SDK](https://github.com/paynl/sdk), so all functions from the original SDK are also available.

### Installation

This SDK uses composer.

Composer is a tool for dependency management in PHP. It allows you to declare the libraries your project depends on and it will manage (install/update) them for you.

For more information on how to use/install composer, please visit: [https://github.com/composer/composer](https://github.com/composer/composer)

To install the Pay.nl PHP SDK-iDin into your project, simply

	$ composer require paynl/sdk-iDin


### Installation without composer 
Coming soon..

### Setting up
To communicate with the API of Pay.nl, you'll need to authenticate.
Pay.nl uses a token to authenticate you. You can find your token in the pay.nl admin. On the bottom of the [API Tokens](https://admin.pay.nl/company/tokens) page.

##### Step 1 the autoloader
Composer generates an autoloader for your application.
To be able to access the classes of the SDK, all you have to do is include the composer autoloader.
The autoloader is located here: vendor/autoload.php

```php
require_once('path_to/vendor/autoload.php');
```

##### Step 2 Your APItoken
To let the SDK know what your APItoken is, you'll have to register the TokenCode (AT-code belonging to the token) and APItoken as follows:

```php
\Paynl\Config::setTokenCode('AT-....-....');
\Paynl\Config::setApiToken('YOUR_API_TOKEN');
```

Now you're ready to make some calls


### Examples

The full list of functions can be found in the [samples](https://github.com/paynl/sdk-iDin/tree/master/samples) folder.



