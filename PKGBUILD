# Script generated with Bloom
pkgdesc="ROS - The swri_transform_util package contains utility functions and classes for transforming between coordinate frames."
url='https://github.com/swri-robotics/marti_common'

pkgname='ros-kinetic-swri-transform-util'
pkgver='2.2.0_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('boost'
'geos'
'pkg-config'
'proj'
'ros-kinetic-catkin'
'ros-kinetic-cv-bridge'
'ros-kinetic-diagnostic-msgs'
'ros-kinetic-dynamic-reconfigure'
'ros-kinetic-geographic-msgs'
'ros-kinetic-geometry-msgs'
'ros-kinetic-gps-common'
'ros-kinetic-nodelet'
'ros-kinetic-roscpp'
'ros-kinetic-rospy'
'ros-kinetic-rostest'
'ros-kinetic-swri-math-util'
'ros-kinetic-swri-nodelet'
'ros-kinetic-swri-roscpp'
'ros-kinetic-swri-yaml-util'
'ros-kinetic-tf'
'ros-kinetic-topic-tools'
'yaml-cpp'
)

depends=('boost'
'geos'
'proj'
'ros-kinetic-cv-bridge'
'ros-kinetic-diagnostic-msgs'
'ros-kinetic-dynamic-reconfigure'
'ros-kinetic-geographic-msgs'
'ros-kinetic-geometry-msgs'
'ros-kinetic-gps-common'
'ros-kinetic-nodelet'
'ros-kinetic-roscpp'
'ros-kinetic-rospy'
'ros-kinetic-sensor-msgs'
'ros-kinetic-swri-math-util'
'ros-kinetic-swri-nodelet'
'ros-kinetic-swri-roscpp'
'ros-kinetic-swri-yaml-util'
'ros-kinetic-tf'
'ros-kinetic-topic-tools'
'yaml-cpp'
)

conflicts=()
replaces=()

_dir=swri_transform_util
source=()
md5sums=()

prepare() {
    cp -R $startdir/swri_transform_util $srcdir/swri_transform_util
}

build() {
  # Use ROS environment variables
  source /usr/share/ros-build-tools/clear-ros-env.sh
  [ -f /opt/ros/kinetic/setup.bash ] && source /opt/ros/kinetic/setup.bash

  # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  # Fix Python2/Python3 conflicts
  /usr/share/ros-build-tools/fix-python-scripts.sh -v 2 ${srcdir}/${_dir}

  # Build project
  cmake ${srcdir}/${_dir} \
        -DCMAKE_BUILD_TYPE=Release \
        -DCATKIN_BUILD_BINARY_PACKAGE=ON \
        -DCMAKE_INSTALL_PREFIX=/opt/ros/kinetic \
        -DPYTHON_EXECUTABLE=/usr/bin/python2 \
        -DPYTHON_INCLUDE_DIR=/usr/include/python2.7 \
        -DPYTHON_LIBRARY=/usr/lib/libpython2.7.so \
        -DPYTHON_BASENAME=-python2.7 \
        -DSETUPTOOLS_DEB_LAYOUT=OFF
  make
}

package() {
  cd "${srcdir}/build"
  make DESTDIR="${pkgdir}/" install
}

