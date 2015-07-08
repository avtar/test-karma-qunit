# Testing Karma and QUnit

This repository contains a very basic QUnit test meant to troubleshoot potential Karma and/or QUnit issues.

## Requirements

* Chrome
* Firefox
* NPM

## Get started

    npm install
    karma start
    karma run

Upon running ```karma start``` Chrome and Firefox should be launched and captured.

## Potential issue(s)

You should get similar output after triggering a test run:

    $ karma run
    [2015-07-08 12:16:27.498] [DEBUG] config - Loading config /home/avtar/projects/test-karma-qunit/karma.conf.js
    Chrome 43.0.2357 (Linux 0.0.0) ERROR
      Uncaught Error: Called start() outside of a test context while already started
      at /home/avtar/projects/test-karma-qunit/tests/lib/qunit/js/qunit.js:287
    Firefox 37.0.0 (Linux 0.0.0): Executed 1 of 1 SUCCESS (0.001 secs / 0.001 secs)

Firefox runs tests and reports results whereas Chrome returns the error above. When trying to use Karma with QUnit for Flocking or Fluid Infusion Chrome returns the following error:

    Uncaught Error: pushFailure() assertion outside test context, was     at F.QUnit.start (/home/avtar/projects/fluid/infusion/tests/lib/qunit/js/qunit.js:465:10)

