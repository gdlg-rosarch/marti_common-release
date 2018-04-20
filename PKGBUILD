# Script generated with Bloom
pkgdesc="ROS - swri_roscpp"


pkgname='ros-lunar-swri-roscpp'
pkgver='2.2.0_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('gtest'
'ros-lunar-catkin'
'ros-lunar-diagnostic-updater'
'ros-lunar-nav-msgs'
'ros-lunar-roscpp'
'ros-lunar-rostest'
'ros-lunar-std-msgs'
'ros-lunar-std-srvs'
)

depends=('ros-lunar-diagnostic-updater'
'ros-lunar-nav-msgs'
'ros-lunar-roscpp'
'ros-lunar-std-msgs'
'ros-lunar-std-srvs'
)

conflicts=()
replaces=()

_dir=swri_roscpp
source=()
md5sums=()

prepare() {
    cp -R $startdir/swri_roscpp $srcdir/swri_roscpp
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

