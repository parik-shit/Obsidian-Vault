### Virtual Function 
- Let's first learn about base class pointer - 
- ##### Base class pointer - 
	It can point to the object of any of its child class. But converse is not true.


```

class A {
	public:
	void f1(){
	cout<<" f1 of A "<<endl;
	}
	
}
class B: public A {
	public:
	void f1(){
	cout<<" f1 of B "<<endl;
	}
	
}

int main(){
	//creating a pointer of type A
	A *p;
	//creating an object of type B
	B obj1;
	//setting Base Class Pointer 
	p = &obj1;
	//invoking f1 using base class pointer 'p'
	p -> f1();
	
}
```

If we look at the above code, we are invoking the function **f1()** using the base class pointer **p** .

### What do we expect to happen ?
Invoking **f1()** of child class **B** , right.

- Output - `f1 of A `

### Reason - 
The unexpected behavior is due to early binding of our program during compile time. Because at the compile time our pointer is allocated memory. By default the type of f1( ) becomes of A, as the pointer is of class A.

###  Fix - 
In order to prevent this behavior, we can use virtual keyword while declaring the function in our parent class.
This will prevent early binding of our pointer. What we need is **late binding** or **dynamic binding ** i.e the memory is allocated during the run time , so that the type of f1() becomes **B** .

```
class A {
	public:
	virtual void f1(){
	cout<<" f1 of A "<<endl;
	}
	
}
class B: public A {
	public:
	void f1(){
	cout<<" f1 of B "<<endl;
	}
	
}
```

- Output - `f1() of B`