# Array
### Definition:
```go
var speed [5]float64 // creates 5 elements with 0 default values in them
```
Empty array that can grow
```go
var slice []int  = make([]int, 5) //creates 5 allocations for now
// we can pass third argument to make for max capacity of array
var slice1 []int = make([]int, 5, 10) // 5 elemens, can hold upto 10
```
Call **len** to get current length (5 in this case), or **cap** for capacity of the array (10 in second example)

### Setting value - individually:
```go
var speed [5]float64
speed[0]=1.2
// up to speed[4]
```
### Setting values - all in one go:
```go
var speed [5]float64 = [5]float64{0.5,1.2,3.1,2.1,1,1} // or
speed := [5]float64{0.5,1.2,3.1,2.1,1,1} // or
speed := [...]float64{0.5,1.2,3.1,2.1,1,1} 
```
### Iterate over array
```
speed := [5]float64{0.1,2.1,3.3,5.5,6.1}
for index,value := range speed {
  // do something
}
```
### Get a slice of an array
```go
distance := [5]int{1,2,3,4,5}
sub := distance[1:3] // start at index 1, stop before index 3
// sub is [2,3] 
//Note len and cap difference
len(sub) // equals 2
cap(sub) // equals 4 (we started at index 1, so it saves 4 spots)
```
Think of cap for sub as a pointer to the index 1 and so it has knowledge of the remaining items in the array, but not before.

### Append Values
```go
distance := [5]int{1,2,3,4,5} 
result := append(distance, 10) // ERROR => distance is const length
// However we can append to:
distance1 := make([]int, 5) // new array
result1 := append(distance1, 10)
// Or we could slice and append like:
distance1 = distance[1:3] // new array
resulet2 = append(distance1, 6,7)
```
Note that append method adds a new item to the end of array
Capacity is doubled when maximum is reached - for sizable arrays (slices and make)