# Week - 9

# Write a GO Program to calculate average using arrays.

```go
package main

import (
	"fmt"
)

func main() {
	arr := [100]int{}
	var arrSize, storeSum, average int

	fmt.Print("Enter the size of the array : ")
	fmt.Scan(&arrSize)

	for i := 0; i < arrSize; i++ {
		fmt.Print("Enter the element : ")
		fmt.Scan(&arr[i])
		storeSum += arr[i]
	}

	average = storeSum / arrSize

	fmt.Print("Average : ", average)
}
```


# Week - 10

# Write a GO program to delete duplicate element in a given array.

```go
package main

import (
	"fmt"
)

func removeDuplicates(arr []int) []int {
	boolDict := make(map[int]bool)
	tempArr := []int{}
	for _, i := range arr {
		if !boolDict[i] {
			boolDict[i] = true
			tempArr = append(tempArr, i)
		}
	}
	return tempArr
}

func main() {
	arr := []int{1, 2, 3, 3, 4}
	fmt.Print(removeDuplicates(arr))
}
```
