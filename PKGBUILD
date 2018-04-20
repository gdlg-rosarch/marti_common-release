# Script generated with Bloom
pkgdesc="ROS - This library provides functionality to simplify working with the navigation messages defined in marti_nav_msgs."


pkgname='ros-lunar-swri-route-util'
pkgver='2.2.0_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('ros-lunar-catkin'
'ros-lunar-marti-common-msgs'
'ros-lunar-marti-nav-msgs'
'ros-lunar-roscpp'
'ros-lunar-swri-geometry-util'
'ros-lunar-swri-math-util'
'ros-lunar-swri-transform-util'
'ros-lunar-visualization-msgs'
)

depends=('ros-lunar-marti-common-msgs'
'ros-lunar-marti-nav-msgs'
'ros-lunar-roscpp'
'ros-lunar-swri-geometry-util'
'ros-lunar-swri-math-util'
'ros-lunar-swri-transform-util'
'ros-lunar-visualization-msgs'
)

conflicts=()
replaces=()

_dir=swri_route_util
source=()
md5sums=()

prepare() {
    cp -R $startdir/swri_route_util $srcdir/swri_route_util
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

