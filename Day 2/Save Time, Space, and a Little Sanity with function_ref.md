David Ledger

- Not in the std yet but there are 3rd party options
- Very small in memory size for copy purposes
- A callable is anything that can be called with std::invoke
	- Lambdas are an example of callables
- std::string_view is an analogous tool
- since it is a reference, you have to ensure that the lifetimes line up properly
- useful in function parameters to avoid creating multiple dispatches when unnecessary
- can super reduce code-size and even improve runtime
- TartanLlama/function_ref has a working implementation