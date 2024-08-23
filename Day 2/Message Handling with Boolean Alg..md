Ben Deane

- fields are a set of (name, type, pointer) and a message is a named collection of fields (name, []fields)
- a matcher is a predicate that operates on a message
	- Can be run at compile-time
	- since a matcher is isomorphic to booleans, we can create "and", "or", and "not" functions that operate on matchers
- a callback is a matcher and a function to call that uses a handler
- Replacing matchers with "atomic" true and false states can help making simplifying easier.