## Test environments
* local macOS High Sierra 10.13.3, R-3.4.4
* Ubuntu 14.04.5 LTS (on travis-ci), R-3.4.4
* win-builder

## R CMD check results

0 errors | 0 warnings | 0 notes

For win-builder:

## Reverse dependencies

There are currently no downstream dependencies for this package.

---

`essurvey` was had a fatal bug documented here: https://github.com/ropensci/essurvey/issues/31. This version fixes the bug.

---

- *Most* examples are wrapped in \dontrun{} because they cannot be run
  in < 5 seconds. No smaller toy examples can be created. Functions
  which can be executed in < 5 are allow to run.

  Also, most functions use personal emails to actually run. Even if using
  \dontshow{} I wouldn’t want to reveal any information (either on Github or
  somewhere on the CRAN repo) of personal use.

- The tests are wrapped skip_on_cran()
  since they absolutely require using a private email. Full tests
  are run on Travis (weekly) with results available for review:
  https://travis-ci.org/ropensci/essurvey
  
  The Travis tests have an environment variable containing the email. This
  allows the tests to run smoothly.