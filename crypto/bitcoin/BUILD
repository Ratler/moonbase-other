if in_depends $MODULE qt5; then
  . /etc/profile.d/qt5.rc
fi &&

OPTS+=" --disable-tests" &&

CXXFLAGS+=" -DBOOST_VARIANT_USE_RELAXED_GET_BY_DEFAULT=1" &&

./autogen.sh &&

default_build
