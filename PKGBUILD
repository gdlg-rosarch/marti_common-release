# Script generated with Bloom
pkgdesc="ROS - swri_image_util"
url='https://github.com/swri-robotics/marti_common'

pkgname='ros-lunar-swri-image-util'
pkgver='2.2.0_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('eigen3'
'pkg-config'
'ros-lunar-camera-calibration-parsers'
'ros-lunar-catkin'
'ros-lunar-cv-bridge'
'ros-lunar-geometry-msgs'
'ros-lunar-image-geometry'
'ros-lunar-image-transport'
'ros-lunar-message-filters'
'ros-lunar-nav-msgs'
'ros-lunar-nodelet'
'ros-lunar-roscpp'
'ros-lunar-rospy'
'ros-lunar-rostest'
'ros-lunar-std-msgs'
'ros-lunar-swri-geometry-util'
'ros-lunar-swri-math-util'
'ros-lunar-swri-nodelet'
'ros-lunar-swri-opencv-util'
'ros-lunar-swri-roscpp'
'ros-lunar-tf'
)

depends=('eigen3'
'ros-lunar-camera-calibration-parsers'
'ros-lunar-cv-bridge'
'ros-lunar-geometry-msgs'
'ros-lunar-image-geometry'
'ros-lunar-image-transport'
'ros-lunar-message-filters'
'ros-lunar-nav-msgs'
'ros-lunar-nodelet'
'ros-lunar-roscpp'
'ros-lunar-rospy'
'ros-lunar-std-msgs'
'ros-lunar-swri-geometry-util'
'ros-lunar-swri-math-util'
'ros-lunar-swri-opencv-util'
'ros-lunar-swri-roscpp'
'ros-lunar-tf'
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

