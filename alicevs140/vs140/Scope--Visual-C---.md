---
title: "Scope (Visual C++)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: language-reference
ms.assetid: 81fecbb0-338b-4325-8332-49f33e716352
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Scope (Visual C++)
C++ names can be used only in certain regions of a program. This area is called the "scope" of the name. Scope determines the "lifetime" of a name that does not denote an object of static extent. Scope also determines the visibility of a name, when class constructors and destructors are called, and when variables local to the scope are initialized. (For more information, see [Constructors](../vs140/Constructors--C---.md) and [Destructors](../vs140/Destructors--C---.md).) There are five kinds of scope:  
  
-   **Local scope** A name declared within a block is accessible only within that block and blocks enclosed by it, and only after the point of declaration. The names of formal arguments to a function in the scope of the outermost block of the function have local scope, as if they had been declared inside the block enclosing the function body. Consider the following code fragment:  
  
    ```  
    {  
        int i;  
    }  
    ```  
  
     Because the declaration of `i` is in a block enclosed by curly braces, `i` has local scope and is never accessible because no code accesses it before the closing curly brace.  
  
-   **Function scope** Labels are the only names that have function scope. They can be used anywhere within a function, but are not accessible outside that function. Formal arguments (arguments specified in function definitions) to functions are considered to be in the scope of the outermost block of the function body.  
  
-   **File scope** Any name declared outside all blocks or classes has file scope. It is accessible anywhere in the translation unit after its declaration. Names with file scope that do not declare static objects are often called global names.  
  
     In C++, file scope is also known as namespace scope.  
  
-   **Class scope** Names of class members have class scope. Class member functions can be accessed only by using the member-selection operators (**.** or **–>**) or pointer-to-member operators (**.\*** or **–>\***) on an object or pointer to an object of that class; nonstatic class member data is considered local to the object of that class. Consider the following class declaration:  
  
    ```  
    class Point  
    {  
        int x;  
        int y;  
    };  
    ```  
  
     The class members `x` and `y` are considered to be in the scope of class `Point`.  
  
-   **Prototype scope** Names declared in a function prototype are visible only until the end of the prototype. The following prototype declares three names (`strDestination`, `numberOfElements`, and `strSource`); these names go out of scope at the end of the prototype:  
  
    ```  
    errno_t strcpy_s( char *strDestination, size_t numberOfElements, const char *strSource );  
    ```  
  
## Hiding Names  
 You can hide a name by declaring it in an enclosed block. In the following figure, `i` is redeclared within the inner block, thereby hiding the variable associated with `i` in the outer block scope.  
  
 ![Block&#45;scope name hiding](../vs140/media/vc38SF1.png "vc38SF1")  
Block Scope and Name Hiding  
  
 The output from the program shown in the figure is:  
  
```  
i = 0  
i = 7  
j = 9  
i = 0  
```  
  
> [!NOTE]
>  The argument `szWhat` is considered to be in the scope of the function. Therefore, it is treated as if it had been declared in the outermost block of the function.  
  
## Hiding class names  
 You can hide class names by declaring a function, object or variable, or enumerator in the same scope. However, the class name can still be accessed when prefixed by the keyword **class**.  
  
```  
// hiding_class_names.cpp  
// compile with: /EHsc  
#include <iostream>  
using namespace std;  
  
// Declare class Account at file scope.  
class Account  
{  
public:  
    Account( double InitialBalance )  
        { balance = InitialBalance; }  
    double GetBalance()  
        { return balance; }  
private:  
    double balance;  
};  
  
double Account = 15.37;            // Hides class name Account  
  
int main()  
{  
    class Account Checking( Account ); // Qualifies Account as   
                                       //  class name  
  
    cout << "Opening account with balance of: "  
         << Checking.GetBalance() << "\n";  
}  
//Output: Opening account with balance of: 15.37  
```  
  
> [!NOTE]
>  Any place the class name (`Account`) is called for, the keyword class must be used to differentiate it from the file-scoped variable Account. This rule does not apply when the class name occurs on the left side of the scope-resolution operator (::). Names on the left side of the scope-resolution operator are always considered class names.  
  
 The following example demonstrates how to declare a pointer to an object of type `Account` using the **class** keyword:  
  
```  
class Account *Checking = new class Account( Account );  
```  
  
 The `Account` in the initializer (in parentheses) in the preceding statement has file scope; it is of type **double**.  
  
> [!NOTE]
>  The reuse of identifier names as shown in this example is considered poor programming style.  
  
 For more information about pointers, see [Derived Types](assetId:///aa14183c-02fe-4d81-95fe-beddb0c01c7c). For information about declaration and initialization of class objects, see [Classes, Structures, and Unions](../vs140/Classes-and-Structs--C---.md). For information about using the **new** and **delete** free-store operators, see [Special Member Functions](../vs140/Special-Member-Functions--C---.md).  
  
## Hiding names with file scope  
 You can hide names with file scope by explicitly declaring the same name in block scope. However, file-scope names can be accessed using the scope-resolution operator (`::`).  
  
```  
// file_scopes.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int i = 7;   // i has file scope, outside all blocks  
using namespace std;  
  
int main( int argc, char *argv[] ) {  
   int i = 5;   // i has block scope, hides i at file scope  
   cout << "Block-scoped i has the value: " << i << "\n";  
   cout << "File-scoped i has the value: " << ::i << "\n";  
}  
```  
  
 **Block-scoped i has the value: 5**  
**File-scoped i has the value: 7**   
## See Also  
 [Basic Concepts](../vs140/Basic-Concepts---C---.md)