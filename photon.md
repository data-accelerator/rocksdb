## Build

```bash
./photon-auto-convert.sh
cmake -B build -D FAIL_ON_WARNINGS=off -D CMAKE_BUILD_TYPE=Release
cmake --build build -t rocksdb -j
cmake --build build -t db_bench -j
```
