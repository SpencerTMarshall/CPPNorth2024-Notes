Tristan Brindle

- Fedor Pikus talk at CPPCon '23
- Check out 'Flux' library at tcbrindle/flux
- Safety is about avoiding the possibility of 'undefined behavior'
	- undefined behavior is handled compiler specific (not nicely)
- std::strong_order() can help you safely sort floats (NaN is not ordered in most languages)
- .at() does bounds-checked array indexing so you don't accidentally go into undefined behavior (some don't as of yet)
	- Flux gives a general function you can use with flux::read_at
	- You don't need to bother when you are using well-travelled algorithms. So most use cases for .at() can be removed with smarter code
	- shnatsel on medium how to avoid bounds checks in rust is a good article to read for other alternatives
- Memory safety is hard because most of the time the code will run perfectly fine but can come up out of nowhere
	- Law of Exclusivity is enough to prevent all memory errors in C++
	- flux::zip helps with this
- Testing is important (google has a testing service that seems popular?)
	- Should look up: Kevlin Henney Program with GUTs (Meeting C++ 2021)
	- constexpr testing
		- If undefined behavior occurs in a constexpr environment, then the compiler is required to log it by the standard
		- can check a constexpr at compile time with static_assert()
		- unit tests will not be able to check for this