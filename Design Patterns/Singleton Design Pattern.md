### Definition

- Two Main Features 
	- One and only one instance of the class
	- Global access to the instance of the class

### Implementation

```Java
package io.sriki;

public class Singleton {

    // for providing the global access, static variable (class variable) is used
    private static Singleton singleton;

    private int first;
    private int second;

    // Singleton classes can only be instantiated using the static method to control the creation of object.
    // so the constructor is private

    private Singleton(){
        this.first=0;
        this.second=10;
    }

    public static Singleton getInstance() {

        // instance is not created yet ( LAZY INSTANTIATION )
        if(singleton == null){
            singleton = new Singleton();
        }
        // if instance is not null, return the instance
        return singleton;
    }

    public int getFirst(){
        return this.first;
    }

    public int getSecond() {
        return this.second;
    }

}

```

-  Both instance variable and constructor  are  <mark style="background: #D2B3FFA6;">private</mark>
-  Both instance variable and *getInstance()* are <mark style="background: #FF5582A6;">static</mark>

![[singletonClassDiagram.png]]