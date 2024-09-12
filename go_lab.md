# Exp - 5 : Floyd's Triangle

```go
package main
import "fmt"

func main() {
    var rows int
    var temp int = 1
    fmt.Print("Enter the no of rows :")
    fmt.Scanln(&rows)
    for i:=0; i<rows; i++{
        for j:=0; j<=i; j++{
            fmt.Printf(" %d", temp)
            temp++
        }
        fmt.Println("")
    }
}
```

# Exp - 6 : Addition of two strings

```go
```

# Exp - 7 : Check whether a number is palindrome or not

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
