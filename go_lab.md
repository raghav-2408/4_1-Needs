# Exp - 1 : Program to find LCM and GCD of given two numbers.

```go


```


# Exp - 2 : Print Pyramid of numbers

```go

package main
import "fmt"

func main() {
    var temp, rows, temp1, k int
    fmt.Scan(&rows)
    for i:=1; i<=rows; i++{
        for j:=1; j<=rows-i; j++{
            fmt.Print(" ")
            temp++
        }
        for{
            if (temp <= rows-1){
                fmt.Printf("%d", i+k)
                temp++
            }else{
                temp1++
                fmt.Printf("%d", (i+k-2*temp1))
            }
            k++
            if(k == (2*i-1)){
                break
            }
        }
        temp = 0
        temp1 = 0
        k = 0
        fmt.Println("")
    }
}
```

# Exp - 3 : Program to use struct that is imported from another package.

```go

```

# Exp - 4 : Calculate Standard Deviation in Math package

```go
package main
import (
    "fmt"
    "math"
    )

func main() {
    var mean, sum, variance, sd float64
    var nums[4] float64
    for i:=0; i<4; i++{
        fmt.Scan(&nums[i])
        sum+=nums[i]
    }
    mean = sum / 4
    
    for i:=0; i<4; i++{
        variance += math.Pow(nums[i] - mean, 2)
    }
    
    sd = math.Sqrt(variance / 4)
    
    fmt.Println(sd)
}
```

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
package main
import "fmt"

func main() {
    var s1, s2 string
    fmt.Print("Enter string 1 : ")
    fmt.Scan(&s1)
    fmt.Print("Enter string 2 : ")
    fmt.Scan(&s2)
    fmt.Println(s1+s2)
}
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
