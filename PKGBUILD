# Script generated with Bloom
pkgdesc="ROS - This library provides functionality to simplify working with the navigation messages defined in marti_nav_msgs."


pkgname='ros-kinetic-swri-route-util'
pkgver='2.2.0_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('ros-kinetic-catkin'
'ros-kinetic-marti-common-msgs'
'ros-kinetic-marti-nav-msgs'
'ros-kinetic-roscpp'
'ros-kinetic-swri-geometry-util'
'ros-kinetic-swri-math-util'
'ros-kinetic-swri-transform-util'
'ros-kinetic-visualization-msgs'
)

depends=('ros-kinetic-marti-common-msgs'
'ros-kinetic-marti-nav-msgs'
'ros-kinetic-roscpp'
'ros-kinetic-swri-geometry-util'
'ros-kinetic-swri-math-util'
'ros-kinetic-swri-transform-util'
'ros-kinetic-visualization-msgs'
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

