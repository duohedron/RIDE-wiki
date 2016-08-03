==================
Test Runner Plugin
==================

Introduction
============

The test runner adds a tab which lets you run robot tests directly within
RIDE. It supports multiple "profiles" (profiles for "pybot" and "jybot" come
with the plugin). It allows you to run an entire suite, or run a subset by
checking a checkbox next to individual tests.

Usage
=====

Once enabled, this plugin adds the following components:

  * Tools menu item "Run Test Suite"
  * Tools menu item "Stop Running"
  * toolbar button to start a test
  * toolbar button to stop a test
  * notebook tab for configuring and running a test

The easiest way to use the plugin is to simply click on the "run" toolbar tool. This will show the Run notebook tab and start running a test against the currently opened suite.

For finer grained control over the test you can select the Run notebook tab, and from there select individual tests to run, and/or add tags to the --include-tags and --exclude-tags options.

Execution Profiles
------------------

The plugin supports the notion of execution "profiles". These profiles appear in the notebook tab as a dropdown list. By default there are three profiles: one for pybot, one for jybot and one for your custom script. Custom script option provides you a field where you can write your script name or browse the script by using the file browser opened through "Browse" button.

If you need more than just running script, you can modify the `runprofiles.py` file in the plugin directory to add more advanced custom profiles. Custom profiles are useful if you have other tools for kicking off a test, or if you want to hard-code a set of command line options.

Test Case Selection
-------------------

The notebook tab includes a hierarchical tree of the test suite, similar to the tree on the left side of RIDE. Through this widget you can check a checkbox next to individual tests. When you click run, only the checked tests will run. There is one special case where if no tests are checked, all tests will be run.

Once a test has been run at least once, a context-sensitive menu over the tree will give you the option to select only the tests that have failed. You can also select or deselect all tests, as well as select/deselect only children of the currently highlighted suite.

The default profiles also let you type in one or more tags to be used either for test selection or for ignoring tests. These lists of tags can be separated either by commas or by vertical bars.

Viewing Test Reports
--------------------

The notebook tab has a window for viewing the stdout of the test process. In addition, there is a progress bar that is animated while a test is run, and an indicator appears next to each test as it is running which changes color once the test has passed or failed. One a test completes, two buttons within the tab allow you to open up a browser for the log or report file.

Details
=======

When you run a test, it will create a temporary directory that matches the pattern RIDE`*`.d in a temporary directory appropriate for each platform. This is where the reports will be written to.

For example, on most linux systems the file would look something like "/tmp/RIDE0u6kgL.d". If RIDE exits normally this directory will be deleted. If RIDE crashes this directory may be left behind. It's perfectly fine to delete these directories at any time (except for deleting the one currently being used).

Screenshots
===========

[[images/testrunner.png]]
