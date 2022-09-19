## Build

```bash
./photon-auto-convert.sh
cmake -B build -D PORTABLE=on -D FORCE_SSE42=on -D FAIL_ON_WARNINGS=off -D WITH_SNAPPY=on -D WITH_LZ4=on -D ENABLE_URING=on -D CMAKE_BUILD_TYPE=Release
cmake --build build -t rocksdb -j
cmake --build build -t perf-client -t perf-server -j
```

P.S. When running CI/db_bench, add -D INIT_PHOTON_IN_ROCKSDB=on
