# Makefile-template

Makefile to be used with my personal C projects.

## Roadmap
- [x] Create Makefile which automatically generates build files from the source files.
- [ ] Add debug option.
- [ ] Add tests.

## Files hierarchy

```bash
.
├── Makefile
├── README.md
├── bin
│   └── main
├── build
│   ├── display.o
│   └── main.o
├── include
│   └── display.h
└── src
    ├── display.c
    └── main.c
```

## Usage

- Place the source files in the `src` folder
- Place the header files in the `include` folder
- Execute the command below to create the `build` and `bin` folders :
```bash
make dir
```
- Execute the command below to create the build files in the `build` folder, and the executable in the `bin` folder :
```bash
make
```

