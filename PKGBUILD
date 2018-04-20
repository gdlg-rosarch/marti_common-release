# Script generated with Bloom
pkgdesc="ROS - swri_image_util"
url='https://github.com/swri-robotics/marti_common'

pkgname='ros-kinetic-swri-image-util'
pkgver='2.2.0_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('eigen3'
'pkg-config'
'ros-kinetic-camera-calibration-parsers'
'ros-kinetic-catkin'
'ros-kinetic-cv-bridge'
'ros-kinetic-geometry-msgs'
'ros-kinetic-image-geometry'
'ros-kinetic-image-transport'
'ros-kinetic-message-filters'
'ros-kinetic-nav-msgs'
'ros-kinetic-nodelet'
'ros-kinetic-roscpp'
'ros-kinetic-rospy'
'ros-kinetic-rostest'
'ros-kinetic-std-msgs'
'ros-kinetic-swri-geometry-util'
'ros-kinetic-swri-math-util'
'ros-kinetic-swri-nodelet'
'ros-kinetic-swri-opencv-util'
'ros-kinetic-swri-roscpp'
'ros-kinetic-tf'
)

depends=('eigen3'
'ros-kinetic-camera-calibration-parsers'
'ros-kinetic-cv-bridge'
'ros-kinetic-geometry-msgs'
'ros-kinetic-image-geometry'
'ros-kinetic-image-transport'
'ros-kinetic-message-filters'
'ros-kinetic-nav-msgs'
'ros-kinetic-nodelet'
'ros-kinetic-roscpp'
'ros-kinetic-rospy'
'ros-kinetic-std-msgs'
'ros-kinetic-swri-geometry-util'
'ros-kinetic-swri-math-util'
'ros-kinetic-swri-opencv-util'
'ros-kinetic-swri-roscpp'
'ros-kinetic-tf'
)

conflicts=()
replaces=()

_dir=swri_image_util
source=()
md5sums=()

prepare() {
    cp -R $startdir/swri_image_util $srcdir/swri_image_util
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

