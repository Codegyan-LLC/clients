<p align="center">
    <img src="https://raw.githubusercontent.com/codegyan/client/main/art/code.png" width="600" alt="Codegyan PHP">
    <p align="center">
        <a href="https://github.com/codegyan/client/actions"><img alt="GitHub Workflow Status (main)" src="https://img.shields.io/github/actions/workflow/status/codegyan/client/tests.yml?branch=main&label=tests&style=round-square"></a>
        <a href="https://packagist.org/packages/codegyan/client"><img alt="Total Downloads" src="https://img.shields.io/packagist/dt/codegyan/client"></a>
        <a href="https://packagist.org/packages/codegyan/client"><img alt="Latest Version" src="https://img.shields.io/packagist/v/codegyan/client"></a>
        <a href="https://packagist.org/packages/codegyan/client"><img alt="License" src="https://img.shields.io/github/license/codegyan/client"></a>
    </p>
</p>

------
**Codegyan PHP SDK** for interacting with the [Codegyan API](https://developer.codegyan.in/docs/). If you or your business relies on this package, it's important to support the developers who have contributed their time and effort to create and maintain this valuable tool:

- Prathmesh Yelne : **[github.com/sponsors/prathmeshyelne](https://github.com/sponsors/prathmeshyelne)**

## Table of Contents
- [Get Started](#get-started)
- [Usage](#usage)
  - [Compiler Resource](#compiler-resource)
  - [Tools Resource](#tools-resource)
  - [Articles Resource](#articles-resource)
  - [tutorials Resource](#tutorilas-resource)
- [Troubleshooting](#troubleshooting)
- [Testing](#testing)
- [Services](#services)

## Get Started

> **Requires [PHP 8.1+](https://php.net/releases/)**

First, install Codegyan via the [Composer](https://getcomposer.org/) package manager:

```bash
composer require codegyan/client
```

Then, interact with Codegyan's API:

```php
use Codegyan\Client;

// Your API key and client ID
$apiKey = '';
$clientId = '';

// Create a Client instance
$client = new Client($apiKey, $clientId);

$domain = "codegyan.in"; // Domain Here 

try {
    $result = $client->toolsApiClient->domainAvailability($domain);
    echo "$result\n";
} catch (Exception $e) {
    echo "Error: " . $e->getMessage() . "\n";
}
```

## Usage
### `Compiler` Resource

The Compiler resource allows you to compile code snippets. Here's an example of how to use it:



```php
use Codegyan\Client;

// Your API key and client ID
$apiKey = '';
$clientId = '';

// Create a Client instance
$client = new Client($apiKey, $clientId);

$lang = "python3";
$code = "print('Hello World')";

try {
    $result = $client->compilerApiClient->compile($lang, $code);
    echo "$result\n";
} catch (Exception $e) {
    echo "Error: " . $e->getMessage() . "\n";
}
```

### `Tools` Resource

The Tools resource provides various utility functions. Here's an example of how to use it:


```php
use Codegyan\Client;

// Your API key and client ID
$apiKey = '';
$clientId = '';

// Create a Client instance
$client = new Client($apiKey, $clientId);

$domain = "example.com";

try {
    $result = $client->toolsApiClient->domainAvailability($domain);
    echo "$result\n";
} catch (Exception $e) {
    echo "Error: " . $e->getMessage() . "\n";
}
```

## Troubleshooting
If you encounter any issues or have any questions, please feel free to reach out to our support team at support@codegyan.com.

## Testing

We highly recommend testing your integration with CodeGyan's PHP SDK to ensure its correctness and reliability. You can use PHPUnit or any other testing framework of your choice to write and execute tests for your application.

If you haven't already installed PHPUnit, you can do so by running:

```bash
composer require --dev phpunit/phpunit
```

Once PHPUnit is installed, you can run your tests using the following command:

```bash
vendor/bin/phpunit
```

This command will execute all tests located in the tests directory of your project.

> Note : Make sure to write tests that cover various use cases and edge cases of your integration with the CodeGyan SDK to ensure robustness.

## Services
For more information about CodeGyan's services, please visit our website.



Codegyan PHP SDK is an open-sourced software licensed under the **[MIT license](https://opensource.org/licenses/MIT)**.