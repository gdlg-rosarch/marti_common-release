^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package swri_route_util
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.1.5 (2016-05-13)
------------------

0.1.4 (2016-05-12)
------------------
* Fix distances in routeDistances for points before start point.
  There were two bugs in routeDistances that were causing the incorrect
  distance to be calculated for points before the start point.  An error
  in the iteration bounds was causing the distance of the first point to
  be 0.0.  Secondly, the arc length for the other points was just the
  relative distance between two points instead of the cummulative
  distance.
* Merge pull request `#331 <https://github.com/evenator/marti_common/issues/331>`_ from elliotjo/sru-add-distance-functions-jade
  Add util functions to calculate distances between route points. (jade)
* Remove commented out code in swri_route_util.
* Add util functions to calculate distances between route points.
  This commit adds two utility functions to calculate the distances (in
  terms of arc length) between route points.  One function calculates
  the distance between two points, the other calculates the distance
  between one point and many other points and should provide much better
  performance for that common need.
* Add native-ish ROS serialization support to sru::Route.
  This commit adds native(-ish) ROS serialization support so that
  swri_route_util::Route can be used directly with publishers and
  subscribers. This is purely for convenience rather than performance
  (although you will get improved performance in nodelets that
  publish/subscribe by avoiding serialization).  Under the hood, the
  implementation does serialization with the native type and then
  converts it to/from the swri_route_util::Route type.
  This commit also fixes a missing special case in
  interpolateRouteSegment (0 < distance < 1) and reorganized the if/else
  blocks to be clearer.
* Add swri_route_util package.
  This commit adds a new package called swri_route_util that provides a
  more user-friendly interface to the marti_nav_msgs Route and RoutPoint
  classes, and a set of useful utilities.  At this point, most of the
  code (except the properties) has been well tested on bag files.
* Contributors: Elliot Johnson, Marc Alban

0.1.3 (2016-03-04)
------------------

0.1.2 (2016-01-06)
------------------

0.1.1 (2015-11-17)
------------------

0.1.0 (2015-09-29)
------------------

0.0.5 (2015-09-27 15:27)
------------------------

0.0.4 (2015-09-27 11:35)
------------------------

0.0.3 (2015-09-26)
------------------

0.0.2 (2015-09-25 15:00)
------------------------

0.0.1 (2015-09-25 09:06)
------------------------
