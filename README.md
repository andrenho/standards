# standards
Programming standards that I follow

# C

- Reinvent the wheel or include contributes source files. Avoid using external libraries. Aim to generate a single executable - the smallest the better.
- Embed data files into the executable. Gzip them.
- Unit tests with TDD
- Isolate OS specific code in source files dedicated only for that. Use posix as default, and emulate posix calls on other OSes
- TODO - error checking and return values

Recommended contributed code:
- JSON parsing: microJSON
- Gzipping: miniz
