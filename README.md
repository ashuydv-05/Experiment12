# Experiment12
## AIM:-
Constructors in C++
## Software used:-
VS code
## Theory:-
A constructor in C++ is a special member function that is used to initialize the variables of a class when an object is created.
### Key Features
1. Name Matching: The constructor's name matches exactly with the class name.
2. No Return Type: Constructors do not have a return type, not even void.
3. Automatic Invocation: A constructor is automatically invoked when an object of the class is instantiated.
4. Initialization: Primarily used to initialize member variables of the class.
### Access Control
1. Public Section: Constructors are typically declared in the public section of a class to allow easy creation of objects.
2. Private or Protected Sections: Can also be declared in the private or protected sections to restrict object creation.
### Constructor Overloading
Multiple Constructors: Constructors can be overloaded, allowing multiple ways of initializing an object.
Restrictions: Constructors cannot be declared as virtual functions.
### Syntax:-
Inside Class Definition:
```
ClassName(parameters) { 
    // implementation 
}
```
### Codes:

1.
```
//ashu yadav
//Prn: 23070123154
#include<iostream>
using namespace std;

class student
{
    int rollno;
    char name[50];
    double fee;
public:
    student()
    {
        cout << "Enter the RollNo: ";
        cin >> rollno;
        cin.ignore();
        cout << "Enter the Name: ";
        cin.getline(name, 50);
        cout << "Enter the Fee: "; 
        cin >> fee;
    }
    void display()
    {
        cout << endl << rollno << "\t" << name << "\t" << fee;
    }
};

int main()
{
    student s; 
    s.display();
    return 0;
}
```
OUTPUT:


![image](https://github.com/user-attachments/assets/22f1b976-d719-43e5-b1a6-7aaf4aabcdc0)


2. 

```
//ashu yadav
//Prn: 23070123154


#include<iostream>
using namespace std;

class student
{
    int rno;
    char name[50];
    double fee;

public:
    student();
    void display();
};
student::student()
{
    cout << "Enter the RollNo: ";
    cin >> rno;
    cout << "Enter the Name: ";
    cin >> name;
    cout << "Enter the Fee: ";
    cin >> fee;
}

void student::display()
{
    cout << endl << rno << "\t" << name << "\t" << fee;
}

int main()
{
    student s;
    s.display();
    return 0;
}
```
OUTPUT:

![image](https://github.com/user-attachments/assets/fddd071c-1b75-4d93-b95f-fa17473385db)


3. 
```
//ashu yadav
//Prn: 23070123154
#include<iostream>
#include<string>
using namespace std;

class Data {
    string name;
    int roll_no;
    char dept[50];
    int batch;

public:
    Data() {
        cout << "Name: ";
        cin >> name;
        cout << "Roll Number: ";
        cin >> roll_no;
        cout << "Department: ";
        cin >> dept;
        cout << "Batch: ";
        cin >> batch;
    }
    void display() {
        cout << endl << "DETAILS:" << endl << name << " " << roll_no << " " << dept << " " << batch << endl;
    }
};

int main() {
    Data d1;
    d1.display();
}
```
Output:

![image](https://github.com/user-attachments/assets/37ff5cc1-4f38-40e3-b816-0a508f6a82d4)

4. 

```
//ashu yadav
//Prn: 23070123154

#include<iostream>
using namespace std;

class Num
{
    public:
    Num(int c, int d)
    {
        if(c>d)
        {
            cout<<c<<" is greater";
        }
        else
        {
            cout<<d<<" is greater";
        }
    }
};

int main()
{
    Num n1(4,3);
    }
```

Output:

![image](https://github.com/user-attachments/assets/2f1ba31a-70d2-4cdf-9b3f-25e4814faab3)

5.
```
//ashu yadav
//Prn: 23070123154

#include<iostream>
#include<string.h>
using namespace std;

class student {
    int rno;
    char name[50];
    double fee;
public:
    student(int no, const char n[], double f);
    student(const student &t);

    void display();
};

student::student(int no, const char n[], double f) {
    rno = no;
    strcpy(name, n);
    fee = f;
}

student::student(const student &t) {
    rno = t.rno;
    strcpy(name, t.name);
    fee = t.fee;
}

void student::display() {
    cout << endl << rno << "\t" << name << "\t" << fee;
}

int main() {
    student s(1001, "Manjeet", 10000);
    s.display();
    student manjeet(s);
    manjeet.display();
    return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/42acef35-a99a-43c1-9435-b8ae6a019ae8)

6.
```
//ashu yadav
//Prn: 23070123154


#include<iostream>
using namespace std;

int count=0;

class destruct
{
    public:
    destruct()
    {
        count++;
        cout<<"No. of objects created: "<<count<<endl;
    }
    ~destruct()
    {
        count--;
        cout<<"No. of objects destroyed: "<<count<<endl;
    }
};

int main()
{
    destruct aa,bb,cc;
    { 
        destruct dd;
    }
    return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/8d79b2f2-f73f-427e-9bef-0e7007d80fa9)


## Conclusion:
In summary, constructors in C++ are essential for initializing objects and ensuring that they start in a valid state. With their automatic invocation upon object creation, lack of a return type, and support for overloading, constructors provide flexibility in object initialization. While typically defined in the public section of a class, they can also be made private or protected to control object creation. Understanding how to effectively define and utilize constructors is fundamental for robust and efficient C++ programming.


