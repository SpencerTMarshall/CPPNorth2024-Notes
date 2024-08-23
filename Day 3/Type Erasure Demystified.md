Fedor Pikus

- type-erasure can help decouple dependencies
- "implementation needs to know the type" "structure does not"
- C++ automates the type-reification, C does not
- some type properties like std::size_t will sometimes be used
- 3 main implementations
	- static functions
		- can move a template parameter of a class from the class template to a constructor function template if possible
		- if you leave the template function arguments without using the template parameter, you can static_cast back and use it without needing to generate extra function code? (ask about this)
	- inheritance
		- Can write an inheriting class that can use the template param freely except for where a scope that shouldn't have information about the template param will obtain information (virtual overrides)
	- v_tables
- Indirection has a cost
	- Well-done type erasure has the same cost as indirection