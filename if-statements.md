# If Statements
### Case 1:
```go
if x < 5 {
  //
} else if {
  //
} else {
  //
}
```
Case 2:
```go
if error:=someFn();error!=nil {
  // run only if error is not nil - error is scoped to this if block only
}
```