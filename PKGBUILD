# Script generated with Bloom
pkgdesc="ROS - Provides wrappers around the yaml-cpp library for various utility functions and to abstract out the API changes made to yaml-cpp between ubuntu:precise and ubuntu:trusty."
url='https://github.com/swri-robotics/marti_common'

pkgname='ros-lunar-swri-yaml-util'
pkgver='2.2.0_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('boost'
'pkg-config'
'ros-lunar-catkin'
'yaml-cpp'
)

depends=('boost'
'yaml-cpp'
)

conflicts=()
replaces=()

_dir=swri_yaml_util
source=()
md5sums=()

prepare() {
    cp -R $startdir/swri_yaml_util $srcdir/swri_yaml_util
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

