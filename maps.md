# Maps
### Initialize:
```go
var classSize map[int]int = make(map[int]int)
classSize[1]=10
classSize[2]=20
```
Go doesn't know exactly how much memory to allocate and so we tell it by using make.

### Initialize with values:
```go
classSize := map[int]int {
  1:10,
  2:20
}
```
### Set value of a specific key:
```go
classSize := map[int]int {
  1:10
}
classSize[1]=100
```
### Get value given a key:
```go
classSize := map[int]int{
  1:10
}
size = classSize[1] // returns 10
size = classSize[10] // returns nil
size, status = classSize[1] // returns 10, true (true == match)
size, status: classSize[10] // returns nil, false (false == no match)
```
### Get given key with if check:
```go
if size, status := classSize[10]; status {
  // status was true so we execute this
}
```