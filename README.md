# Experiment-13
# Aim
To study and implement Constructor Overloading
# Theory

In C++, we can have multiple constructors with the same name as long as they each have a different set of arguments.This is known as Constructor Overloading. It is similar to function overloading. 
Constructor overloading in object-oriented programming enables a class to have multiple constructors with the same name but different parameters. This means that you can create objects in various ways by passing different numbers or types of arguments. The program automatically selects the appropriate constructor based on the arguments provided, making it simple to create and initialize objects.
CODES:

1. 
```
#include<iostream>
using namespace std;
class room
{
    private: 
    double length, breadth;
    public:
    room()
    {
        length = 8.2;
        breadth = 2.2;
    }
    room(double l, double b)
    {
        length = l;
        breadth = b; 
    }
    room(double len)
    {
        length = len;
        breadth = 4.2;
    }
    double calculateArea()
    {
        return length * breadth;
    }
};
int main()
{
    room room1;
    cout << "When no argument is passed:" << endl;
    cout << "Area of room = " << room1.calculateArea() << endl;
    room room2(8.2, 2.2);
    cout << "\nWhen (8.2, 2.2) is passed:" << endl;
    cout << "Area of room = " << room2.calculateArea() << endl;
    room room3(4.2);
    cout << "\nWhen breadth is fixed to 4.2 and (4.2) is passed:" << endl;
    cout << "Area of room = " << room3.calculateArea() << endl;
    return 0;
}
```

O/P:

![image](https://github.com/user-attachments/assets/b8ad6add-291b-43f8-b797-97bae1b72d03)


2.
```
#include <iostream>
using namespace std;
class fetch{
int num;
public:
fetch()

{
    num=7;
   
}
fetch (int x){
    num=x;
}
fetch (fetch& b)
{
    num=b.num;
}
void disp(){
    cout<<num<<endl;
}
};
int main(){
    fetch f1;
    f1.disp();
    fetch f2;
    f2.disp();
    fetch f3;
    f3.disp();
}
```
O/P:

![image](https://github.com/user-attachments/assets/e18b7a8e-4130-460e-93e1-b6c4db7194ad)


# Conclusion
In the codes constructor overloading is demonstrated. The class has three constructors that initialize objects in different ways: a default constructor, a parameterized constructor with two parameters, and a parameterized constructor with one parameter. This shows how constructors can be overloaded to provide multiple ways to initialize an object's attributes. The main() function demonstrates how each constructor defines the length and breadth of a room object and calculates its area accordingly.
