##### Resources
1. Go By Example : https://gobyexample.com 
2. 


Sample Code
```Go
package main

import (
	"fmt"
)

func main () {

	/* 
		Simple Hello World
	*/
	fmt.Println("Hello World")

	/*
		Data types
	*/
	// string
	fmt.Println("go"+"lang")
	// integer
	fmt.Println("1+1=",1+1)
	// string concatination : , adds a space in output
	fmt.Println("this","is","nice")
	// float
	fmt.Println("8.0/3.0 =",8.0/3.0)
	//boolean
	fmt.Println(true && false)

	/*
		Variables
		only declaration : var <name> <type>
	*/
	var a int
	fmt.Println(a)

	var b string = "hello"
	fmt.Println(b)

	c := "wall"
	fmt.Println(c)

	d,e := "my","way"
	fmt.Println(d,e)

	/*
		Constant
	*/
	const f string = "Constant_String"
	//f="invalid_operation"
	fmt.Println(f);

}

```