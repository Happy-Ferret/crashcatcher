Very minimal PoC breakpad crash collector/processor in Go.

Requirements:

* C++ compiler (for breakpad)
* Go compiler

1. Build breakpad "minidump stackwalk" (for processing crashes)
```
  ./bin/build_breakpad.sh
```

2. Run tests and build crashcatcher
```
  go test
  go build
```

3. Run crashcatcher (data is stored in ```./crashdata```)
```
  ./crashcatcher
```

4. Submit test crashes (test data is stored in ```./testdata```)
```
  ./bin/submit.sh 
```

crashcatcher can also be run in "collect only" or "process only" modes,
see:
```
  ./crashcatcher --help
```
for details.
