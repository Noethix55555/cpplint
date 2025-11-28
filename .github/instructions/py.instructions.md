---
applyTo: "*.py"
---
## Addition of unit tests
- Unit tests should exercise each *structural* part of a regex pattern at least once, but should not exhaustively enumerate every alternative within a single alternation.
  - Do <em>not</em> add a new test case if its only difference from an existing test case is that it uses a different word drawn from the same `...|...|...` group in a regex that is already covered by another test.

For example, if a regex applies to both `std::pair<int,int>` and `std::vector<int>` in the same pattern, it is appropriate to have separate test cases for these two. However, once those are covered, a test that only adds `std::list<int>` (where the regex uses `vector|list`) is redundant and should <em>not</em> be added, because it does not exercise any new part of the regex structure—only another alternative of an already tested group.
