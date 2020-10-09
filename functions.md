# Functions
### Case 1:
```go
func someFunc(value: int) int {
  //do some work
  // must return a number
}
```
Takes in integer value and returns integer value

### Case 2:
```go
func someFunc(value: int) (int,int) {
  // do some work
  // return 2 values
  return 1,2
}
```

### Case 3:
```go
func someFunc(value: int) (first: int, second: int) {
  first = 5
  second = 6
  return first, second
}

// call:
// valA, valB := someFunc(0)
```

### Case 4:
```go
func someFunc(value int) (first: int, second: int) {
  first = 5;
  second = 6;
  return
}

// call:
// valA, valB := someFunc(0)
```

### Case 5:
```go
func someFunc(values: ...int) int {
  // do something
  for _, value := range values {
    // do something with value
  }
  // return something - maybe sum?
  return 100
}

// call:
// someFunc(1,2,3,4,5,6) or someFunc(1,2,3) ... etc
```