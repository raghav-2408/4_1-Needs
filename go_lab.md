# Floyd's Triangle

```go
```

# Check whether a number is palindrome or not

```go
package main
import "fmt"
func main(){
	var num, rem, temp int
	var rev int = 0
	num = 4541
	temp = num
	for{
	    rem = num % 10
	    rev = rev * 10 + rem
	    num = num / 10
	    if (num == 0) {
	        break
	    }
	}
	if (temp == rev){
	    fmt.Println("Yes")
	}else{
	    fmt.Println("No")
	}
}
```
