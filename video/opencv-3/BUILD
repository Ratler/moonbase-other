if in_depends $MODULE qt5; then
  . /etc/profile.d/qt5.rc
else
  if in_depends $MODULE qt4; then
    . /etc/profile.d/qt4.rc
  else
    OPTS+=" -DWITH_QT=0"
  fi
fi &&

# bug: examples have to be build, if they (the sources) will be installed
if [[ "`get_module_config EXAMPLES`" = "y" ]]; then
  OPTS+=" -DBUILD_EXAMPLES=1"
else
  OPTS+=" -DBUILD_EXAMPLES=0"
fi &&

OPTS+=" -DBUILD_WITH_DEBUG_INFO=0 \
        -DBUILD_TESTS=0 \
        -DBUILD_PERF_TESTS=0 \
        -DBUILD_SHARED_LIBS=1 \
        -DBUILD_WITH_DYNAMIC_IPP=1 \
        -DOPENCV_EXTRA_MODULES_PATH="../opencv_contrib-$VERSION2/modules" \
        -DCMAKE_SKIP_RPATH=1" &&

default_cmake_build
