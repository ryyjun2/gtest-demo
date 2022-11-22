### Add googletest
```
# https://github.com/google/googletest/blob/main/googletest/README.md

git clone https://github.com/google/googletest.git
```

### Building
```
mkdir build
cd build
cmake ..
make -j2
```

### Run unittest
```
cd build/test
./myunittest
```