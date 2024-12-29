# Silent Map Access Errors in Go

This example demonstrates a common pitfall in Go when working with maps: accessing a key that doesn't exist doesn't result in a runtime panic.  Instead, Go silently returns the zero value for the map's value type.

This can lead to subtle bugs that are difficult to track down because there's no immediate indication that the key is missing.

**File: bug.go** demonstrates the issue.  **File: bugSolution.go** provides a solution using the comma ok idiom.