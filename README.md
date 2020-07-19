# US ZIP Code to State

Some payment providers require a state to be sent when the cardholder is based in the United
States. Rather than add an additional field to our payment form we created this mapping based on
data obtained from https://simple.wikipedia.org/wiki/List_of_ZIP_Code_prefixes.

Usage:

```php
$state = (new \On2Media\UsZipCodeToState\UsZipCodeToState())->getState('90210'); // `CA`
```

Exceptions are thrown if the ZIP code is not five numeric characters or if no match is found.

In addition to state abbreviations (AK, AL, AR, AZ, CA, CO, CT, DE, FL, GA, HI, IA, ID, IL, IN,
KS, KY, LA, MA, MD, ME, MI, MN, MO, MS, MT, NC, ND, NE, NH, NJ, NM, NV, NY, OH, OK, OR, PA, RI,
SC, SD, TN, TX, UT, VA, VT, WA, WI, WV, WY) the following other codes are also returned:

- Armed Forces (AA, AE, AP)
- District of Columbia (DC)
- Territories (GU, PR, VI)
