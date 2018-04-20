# Script generated with Bloom
pkgdesc="ROS - The swri_transform_util package contains utility functions and classes for transforming between coordinate frames."
url='https://github.com/swri-robotics/marti_common'

pkgname='ros-lunar-swri-transform-util'
pkgver='2.2.0_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('boost'
'geos'
'pkg-config'
'proj'
'ros-lunar-catkin'
'ros-lunar-cv-bridge'
'ros-lunar-diagnostic-msgs'
'ros-lunar-dynamic-reconfigure'
'ros-lunar-geographic-msgs'
'ros-lunar-geometry-msgs'
'ros-lunar-gps-common'
'ros-lunar-nodelet'
'ros-lunar-roscpp'
'ros-lunar-rospy'
'ros-lunar-rostest'
'ros-lunar-swri-math-util'
'ros-lunar-swri-nodelet'
'ros-lunar-swri-roscpp'
'ros-lunar-swri-yaml-util'
'ros-lunar-tf'
'ros-lunar-topic-tools'
'yaml-cpp'
)

depends=('boost'
'geos'
'proj'
'ros-lunar-cv-bridge'
'ros-lunar-diagnostic-msgs'
'ros-lunar-dynamic-reconfigure'
'ros-lunar-geographic-msgs'
'ros-lunar-geometry-msgs'
'ros-lunar-gps-common'
'ros-lunar-nodelet'
'ros-lunar-roscpp'
'ros-lunar-rospy'
'ros-lunar-sensor-msgs'
'ros-lunar-swri-math-util'
'ros-lunar-swri-nodelet'
'ros-lunar-swri-roscpp'
'ros-lunar-swri-yaml-util'
'ros-lunar-tf'
'ros-lunar-topic-tools'
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
  [ -f /opt/ros/lunar/setup.bash ] && source /opt/ros/lunar/setup.bash

  # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  # Fix Python2/Python3 conflicts
  /usr/share/ros-build-tools/fix-python-scripts.sh -v 2 ${srcdir}/${_dir}

  # Build project
  cmake ${srcdir}/${_dir} \
        -DCMAKE_BUILD_TYPE=Release \
        -DCATKIN_BUILD_BINARY_PACKAGE=ON \
        -DCMAKE_INSTALL_PREFIX=/opt/ros/lunar \
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

