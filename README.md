# standards
Programming standards that I follow

# C

- Reinvent the wheel or include contributes source files. Avoid using external libraries. Aim to generate a single executable - the smallest the better.
- Start with a complete set of warnings. Remove them if they create much trouble.
- Embed data files into the executable. Gzip them.
- Unit tests with TDD
- Isolate OS specific code in source files dedicated only for that. Use posix as default, and emulate posix calls on other OSes
- Subsystems should be as isolated as possible
- Use OO style when it make sense, avoid global unless is for fixed data.
- TODO - _GNU_SOURCE (?)
- TODO - how to ensure compatibility with all OSes/compilers (?)
- TODO - error checking and return values (?)

Recommended contributed code:
- JSON parsing: microJSON
- Gzipping: miniz

Make should have the following rules:
- all: generate the smallest, fastest executable possible
- dev: build fast (low warnings) with all debugging information
- leaks: check for leaks (valgrind)
- threads: check for error in threads (drd or helgrind)
- check: run unit tests
- check-leaks, check-threads: run these tools on the unit tests
