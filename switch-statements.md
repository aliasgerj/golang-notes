# Switch Statement
### Case 1:
```go
var value int
switch value {
  case 1:
  //
  case 2:
  //
  default:
  ///
}
```

### Case 2:
```go
var value int
switch {
  value < 5:
  //
  value >10
  //
  default:
  //
}
```

### Case 3:
```go
var value string
switch value {
  case '...', '...':
  // Or statement - one or the other
  default:
  //
}
```

case 4:
```go
var value string
switch value {
  case '...':
  //do something
  fallthrough
  case '...':
  // do something
  default: 
  // do something
}
```
By default, switch statement case matches stops matching for more. Adding **fallthrough** allows the code to continue matching for more cases (similar to omitting break in other languages).