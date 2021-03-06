---
theme: base
marp: true
---

<style>
section {
    font-family: Arial, Helvetica, sans-serif;
}
section h1 {
    color: #00A29C;
}
section h2 {
    color: #00A29C;
}
</style>

# go

## Basic Syntax

Pallat Anchaleechamaikorn
Go Developer

yod.pallat@gmail.com
https://github.com/pallat

https://tour.golang.org/
https://github.com/uber-go/guide

---

## Array

var name [n]T

```go
    var array [5]string
```

---

## Array auto counting

var name [n]T

```go
    primes := [...]int{2, 3, 5, 7, 11, 13}    

```

---

## Foreach in Array

var name [n]T

```go
    primes := [...]int{2, 3, 5, 7, 11, 13}

    for i := range primes {
        fmt.Println(primes[i])
    }
```

---

## Foreach index & value

var name [n]T

```go
    primes := [...]int{2, 3, 5, 7, 11, 13}

    for i, prime := range primes {
        fmt.Println(i, prime)
    }
```

---

## Slice

var name []T

```go
    var slice []int

    primes := [...]int{2, 3, 5, 7, 11, 13}    
    slice = primes[1:4]

    for i := range slice {
        fmt.Println(slice[i])
    }
```

---

## Zero value of slice is nil

```go
    var s []int

    if s == nil {
        fmt.Println("it's nil")
    }

// make it first
    s := make([]int, 5)
```

---

## append slice

```go
    s := []int{1, 2, 3, 4, 5}
    s = append(s, 6, 7, 8)
```

---

## Exercise: couple

"abcdef" -> []string{"ab","cd","ef"}
"abcdefg" -> []string{"ab","cd","ef","g*"}

---

## Exercise: moretypes/18

https://tour.golang.org/moretypes/18 https://tour.golang.org/moretypes/18
https://go-tour-th.appspot.com/moretypes/18 https://go-tour-th.appspot.com/moretypes/18

---

## Variadic function (Variable number of arguments)

func variadic(nums ...int)

---

## Spread operator

```go
func variadic(nums ...int) {
    
}

var slice = []int{1, 3, 5, 7, 9}
variadic(slice...)

```

---

## map[T]T

```go
    var m map[string]string
```

---

## zero value of map is nil

```go
    var m map[string]string

    if m == nil {
        fmt.Println("it's nil")
    }
```

---

## map need home

### make

```go
    m := make(map[string]string)

    if m == nil {
        fmt.Println("it's nil")
    }

    m["a"] = "apple"
    m["b"] = "banana"
    m["c"] = "coconut"
    m["d"] = "durian"
    m["e"] = "elderberry"
    m["f"] = "fig"
    m["g"] = "guava"
```

---

## construct map

```go
    m := map[string]string{
        "a" : "apple",
        "b" : "banana",
        "c" : "coconut",
        "d" : "durian",
        "e" : "elderberry",
        "f" : "fig",
        "g" : "guava",
    }

    for k, v := range m {
        fmt.Println(k, v)
    }
```

---

## delete a key

```go
    m := map[string]string{
        "a" : "apple",
        "b" : "banana",
        "c" : "coconut",
        "d" : "durian",
        "e" : "elderberry",
        "f" : "fig",
        "g" : "guava",
    }

    delete(m, "d")

    for k, v := range m {
        fmt.Println(k, v)
    }
```

---

## Exercise: map

open a file oscar_age_male.csv

https://github.com/focusive/go102/tree/master/testdata

print any actors name who got the oscar more than one time

```txt
    Marlon Brando
    Daniel Day-Lewis
    Sean Penn
    Tom Hanks
    Fredric March
    Spencer Tracy
    Gary Cooper
    Jack Nicholson
    Dustin Hoffman
```

