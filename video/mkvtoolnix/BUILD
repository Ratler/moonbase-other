CFLAGS+=" -DBOOST_FILESYSTEM_VERSION=3" &&
CXXFLAGS+=" -DBOOST_FILESYSTEM_VERSION=3" &&

# Temporary define to build against boost 1.58
CXXFLAGS+=' -DBOOST_CODECVT_DO_LENGTH_CONST=const' &&

if in_depends $MODULE qt5; then
  . /etc/profile.d/qt5.rc
fi &&

default_config &&
./drake -j${MAKES} &&

prepare_install &&
./drake install
