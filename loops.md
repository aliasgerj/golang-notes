# Loops
### Case 1:
```go
for i:=1;i<100;i++ {
  //
}
```
### Case 2:
```go
for i <=100 {
  // do something
  i+=1
}
```
Behaves like a while loop

### Case 3:
```go
var statement = "Some statement"
for index, letter := range statement {
  // range ==> i'm iterating over -- statement
  //index is the number, letter is the byte value
  // Use string(letter) to get the actual string value
  // must use both index and letter
}
```
### Case 4:
```go
var statement = "Some statement"
for _, letter := range statement {
  // use _ to tell go we don't intent to use that variable
  // we must use letter in this body
}
```