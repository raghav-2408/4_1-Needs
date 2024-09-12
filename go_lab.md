# Exp - 1 : Program to find LCM and GCD of given two numbers.

```go
package main
import "fmt"

    func lcm(temp1 int, temp2 int) {
        var res int = 1
        if (temp1>temp2){
            res = temp1
        }else{
            res = temp2
        }
        for {
            if (res % temp1 ==0 && res % temp2 == 0){
                fmt.Println("LCM : ", res)
                break
            }
            res++
        }
        return
    }
    
    func gcd(temp1 int, temp2 int){
        var res int = 1
        for i:=1; i<=temp1 && i<=temp2; i++{
            if (temp1%i ==0 && temp2%i==0){
                res = i
            }
        }
        fmt.Print("GCD : ", res)
        return
    }
func main() {
    var n1, n2 int = 3, 6
    var choice int
    fmt.Scan(&choice)
    switch choice{
        case 1 : lcm(n1, n2)
        case 2 : gcd(n1, n2)
        default : fmt.Print("Invalid input")
    }
}
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


`main.go`
```go
package main

import (
	parent "family/father"
	child "family/father/son"
	"fmt"
)

func main() {
	f := new(parent.Father)
	fmt.Println(f.Data("Jim"))

	c := new(child.Son)
	fmt.Print(c.Data("John"))
}
```
`father.go`
```go
package father

import "fmt"

func init() {
	fmt.Println("Father package initialized...")
}

type Father struct {
	Name string
}

func (f Father) Data(name string) string {
	f.Name = "Father : " + name
	return f.Name
}
```

`son.go`

```go
package son

import "fmt"

func init() {
	fmt.Println("Son package initialized...")
}

type Son struct {
	Name string
}

func (s Son) Data(name string) string {
	s.Name = "Son : " + name
	return s.Name
}
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
