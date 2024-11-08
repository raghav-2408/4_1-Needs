# Week - 8

# Write a GO program to build a Contact form.

`main.go`
```go
package main

import (
	"fmt"
	"html/template"
	"net/http"
)

type ContactDetails struct {
	Email   string
	Subject string
	Message string
}

func main() {
	tmpl := template.Must(template.ParseFiles("index.html"))

	http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
		if r.Method != http.MethodPost {
			tmpl.Execute(w, nil)
			return
		}

		details := ContactDetails{
			Email:   r.FormValue("email"),
			Subject: r.FormValue("subject"),
			Message: r.FormValue("message"),
		}

		fmt.Println("Email : ", details.Email)
		fmt.Println("Subject : ", details.Subject)
		fmt.Println("Message : ", details.Message)

		_ = details

		tmpl.Execute(w, struct{ Success bool }{true})
	})

	http.ListenAndServe(":8080", nil)
}
```

`index.html`

```html
{{if .Success}} 
    <h1>Thanks for your message!</h1> 
{{else}} 
    <h1>Contact</h1> 
    <form method="POST"> 
    <label>Email:</label><br /> 
    <input type="text" name="email"><br /> 
    <label>Subject:</label><br /> 
    <input type="text" name="subject"><br /> 
    <label>Message:</label><br /> 
    <textarea name="message"></textarea><br /> 
    <input type="submit"> 
    </form> 
{{end}}
```

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

# Week - 11

# Write a GO program with an example of Array reverse sort Functions for integers and strings.

```go
package main

import (
	"fmt"
	"sort"
)

func main() {
	arr := []int{1, 2, 3, 4}
	sort.Sort(sort.Reverse(sort.IntSlice(arr)))
	fmt.Println("Reversed Array : ", arr)

	str := []string{"apple", "ball", "dog", "cat"}
	sort.Sort(sort.Reverse(sort.StringSlice(str)))
	fmt.Print("Reversed String : ", str)
}
```

# Week - 12

# Write a program comprising of Contains, ContainsAny, Count, EqualFold String Functions.

```go
package main

import (
	"fmt"
	"strings"
)

func main() {
	fmt.Println(strings.Contains("Kim Jong Un", "Jong"))           //true
	fmt.Println(strings.ContainsAny("Kim Jong Un", "im"))          // true
	fmt.Println(strings.Count("Kim Jong Un", "Jong"))              // 1
	fmt.Println(strings.EqualFold("Kim Jong Un", "Yoon Suk Yeol")) // false
}
```

# Week - 14

# Write a GO program to create multiple goroutines and implement how the goroutines scheduler behaves with three logical processors for CRUD using MySQL fromm Scratch.


```go
```
