^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package applanix_bridge
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.0.1 (2014-09-04)
------------------

0.0.0 (2014-09-04)
------------------
* Adding install targets
* Replaced the gps_utm.py with a call to geodesy.utm. Should work, but not
  well tested.
* Cleaned up the dependencies from applanix_bridge
* Changing maintainer of the applanix modules to be me
* Fixed package names in launch file
* Removed a bunch of the chunky comments from the CMakeLists.txt for all
  of the sub projects.
* Moved the smoke test into the applanix_bridge package.
  It seems to work. At the very least it passes, though it does spit out a
  bunch of warnings.
* Moved mapping.py back to applanix_msgs because it's needed by
  applanix_bridge and it makes more sense for it to be there. Also updated
  applanix_bridge to use the new applanix_srvs package.
* Updated applanix_msgs to generate messages so that applanix_bridge can
  use them.
* Making applanix_bridge into a proper rospy package that you can run. Can
  now run things, though they fail because of the missing applanix_msgs.
  Also note that I've removed a bunch of the dependencies until I can
  figure out how to do those properly.
* First stage of catkinizing: catkin metapackage, and consolidate the
  python stuff into applanix_bridge. Have yet to update the CMakeLists.txt
  for the applanix_bridge package to work properly. Also need a setup.py
* Fixed translator for use in Hydro. Seems to work in testing on the Tango
  Tasmania platform.
* Switch the translator to use separate genpy package.
* Adding capture file and basic smoke test to driver.
* Moving gps_utm file to correct package.
* Added some minimal documentation to the manifests, moved publisher to its own package.
* Adding code headers to everything.
* Now publishing the origin of our UTM coordinates wrt. the UTM zone zero point
* Small cleanup of unnecessary shebangs, etc.
* Adding option to autoset a UTM origin
* Added params for base gnss setup.
* Adding COM port configuration
* Adding translation node to convert Applanix messages into standard ROS messages
* Stomped on merge changes. 'master' should now match 'work'.
* Merge branch 'work'
* rename applanix_ctl to applanix_generated_msgs
* Auto-subscribe now working.
* Add nav_mode messages every 5s to keep connection alive.
* Working COM port params.
* Initial support for services.
* Last commit before refactoring to separate thread class per socket.
* Add remaining groups, change the array serialization strategy.
* First commit.
* Contributors: Administrator, Alex Bencz, Kareem Shehata, Mike Purvis, Ryan Gariepy