if in_depends $MODULE openssl || in_depends $MODULE libressl; then
  export PYCURL_SSL_LIBRARY="openssl"
fi &&

make &&

python setup.py build $OPTS &&

prepare_install &&

python setup.py install
