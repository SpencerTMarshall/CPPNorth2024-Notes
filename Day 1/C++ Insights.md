Andreas Fertig

- Compiler Explorer is a good way to find template code
	- C++ insights is linked on Compiler Explorer
- The code C++ Insights shows you compiles in C++, but makes things more explicit and removes a lot of the idiomatic steps. (Can build locally at andreasfertig/cppinsights)
- Uses Clang's AST
	- Doesn't show optimizations
	- libstdc++ and libc++ are supported
	- Some super new features may not be present (tries to use latest release version of Clang)
- Templates don't work cleanly with the application.
- Has different transformation types
- Quick "insights" that the tool gives
	- Stick to simple types if any for default parameters (the AST does not show optimizations)
	- Padding will add "space" to fill types to maintain alignment for erasing and probably some other purposes
		- Can present an issue if alignment cannot be maintained (good to check ?)
	- Can catch undefined behaviour through the object lifetime filter
	- Parentheses don't give lifetime extensions