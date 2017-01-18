# US ZIP Code to State

Some payment providers require a state to be sent when the cardholder is based in the United
States. Rather than add an additional field to our payment form we created this mapping based on
data obtained from https://simple.wikipedia.org/wiki/List_of_ZIP_Code_prefixes.

Usage:

```php
$state = (new \On2Media\UsZipCodeToState\UsZipCodeToState())->getState('90210'); // `CA`
```
