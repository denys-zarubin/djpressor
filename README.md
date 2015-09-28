# djpressor

Using Impressor [![npm version](https://badge.fury.io/js/impressor.svg)](http://badge.fury.io/js/impressor)

### Tests

<a href="https://travis-ci.org/FundedByMe/djpressor"><img src="https://travis-ci.org/FundedByMe/djpressor.svg?branch=master"/></a>
[![Sauce Test Status](https://saucelabs.com/buildstatus/fundedbyme)](https://saucelabs.com/u/fundedbyme)

[![Sauce Test Status](https://saucelabs.com/browser-matrix/fundedbyme.svg)](https://saucelabs.com/u/fundedbyme)

### Running tests

```bash
$ pip install -r tests/requirements.txt
$ py.test tests/
```

To run Selenium tests locally instead of SauceLabs:

```bash
$ RUN_TESTS_LOCAL="True" py.test tests/
```

By default, local Selenium tests will run with PhantomJS.

To change that, edit `tests/test_js.py`:

```python
if RUN_LOCAL:
    # could add Chrome, PhantomJS etc... here
    browsers = ['PhantomJS']
else:
    from sauceclient import SauceClient
    # ...
```
