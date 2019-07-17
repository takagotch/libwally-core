### libwally-core
---
https://github.com/ElementsProject/libwally-core

```
```

```sh
./tools/autogen.sh
./configure <options - see below>
make
make check

./configure --enable-debug --enable-export-all --enable-swig-python --enable-java --enable-coverage
pip install .
pip install wallycore-0.7.2-cp27-cp27mu-linux_x86-linux_x86_64.whl

export ANDROID_HOME=/opt/android-sdk
. ./tools/android_helpers.sh
android_get_arch_list
./tools/cleanup.sh
./tools/autogen.sh
android_build_wally armeabi-v7a $ANDROID_NDK/toolchains/llvm/prebuilt/prebuilt/linux-x86_64 19 "--enable-swig-java"

./tools/cleanup.sh
./tools/cleanup.sh
./tools/autogen.sh
./configure --enable-debug --enable --enable-export-all --enable-swig-python --enable-swig-java --enable-coverage
make
./tools/coverage.sh clean
make check
./tools/coverage.sh
```

