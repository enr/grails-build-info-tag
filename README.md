Build Info Tag Plugin
=====================

This Grails plugin puts a build.info file in the classpath and provides a some GSP tags to display
the information in it.

For now, the build number is the date and the plugin also collects the GIT commit number.

For system with `git` executable in PATH, the plugin calls it.

If Git is not directly callable, the manually parses the refs file or reads the environment variable `GIT_COMMIT`

## Installation

Put in app BuildConfig plugin dependencies:

    compile ":build-info-tag:0.3"

## Tags

* build:buildInfo : provides a list of all properties
* build:buildDate: provides only the value of the buildDate property
* build:gitCommit: provides only the value of the gitCommit property
* build:systemName: provides only the value of the systemName property
* build:timezone: provides only the value of the timezone property

