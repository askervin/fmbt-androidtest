fmbt-androidtest
================

This example demonstrates generating and running tests against the
Phone application on Android.


Prerequisites
-------------

- Install fMBT, version 0.9 or later is required.

- Install Android SDK.

- Launch Nexus-S emulator.

- If everything is ok, you can open Nexus-S screenlock by executing:

$  python -c 'import fmbtandroid; fmbtandroid.Device().swipe((.5, .8), "east")'


Running a test
--------------

- Navigate to the homescreen on Nexus-S.

- Make sure there are no phone calls.

- Launch the test:

$ fmbt -l test.log regressiontest.conf


Debugging a test
----------------

d.enableVisualLog(...) in phone.aal starts logging whatever happens in
the Device instance. The log is written to devicelog.html. Open the
log with your browser:

$ chromium devicelog.html


Model & adapter design
----------------------

See the model & adapter:

$ fmbt-editor phone.aal

Phone.aal enables testing

- activating and backgrounding the phone application.

- calling, two simultaneous calls at max.

- putting calls on hold, switching between two calls.

- hanging up calls in any order.
