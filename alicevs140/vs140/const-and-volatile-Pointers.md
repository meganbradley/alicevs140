---
title: "const and volatile Pointers"
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
ms.topic: article
ms.assetid: 0c92dc6c-400e-4342-b345-63ddfe649d7e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# const and volatile Pointers
The [const](../vs140/const--C---.md) and [volatile](../vs140/volatile--C---.md) keywords change how pointers are treated. The **const** keyword specifies that the pointer cannot be modified after initialization; the pointer is protected from modification thereafter.  
  
 The `volatile` keyword specifies that the value associated with the name that follows can be modified by actions other than those in the user application. Therefore, the `volatile` keyword is useful for declaring objects in shared memory that can be accessed by multiple processes or global data areas used for communication with interrupt service routines.  
  
 When a name is declared as `volatile`, the compiler reloads the value from memory each time it is accessed by the program. This dramatically reduces the possible optimizations. However, when the state of an object can change unexpectedly, it is the only way to ensure predictable program performance.  
  
 To declare the object pointed to by the pointer as **const** or `volatile`, use a declaration of the form:  
  
```  
const char *cpch;  
volatile char *vpch;  
```  
  
 To declare the value of the pointer — that is, the actual address stored in the pointer — as **const** or `volatile`, use a declaration of the form:  
  
```  
char * const pchc;  
char * volatile pchv;  
```  
  
 The C++ language prevents assignments that would allow modification of an object or pointer declared as **const**. Such assignments would remove the information that the object or pointer was declared with, thereby violating the intent of the original declaration. Consider the following declarations:  
  
```  
const char cch = 'A';  
char ch = 'B';  
```  
  
 Given the preceding declarations of two objects (`cch`, of type **const char**, and `ch`, of type **char)**, the following declaration/initializations are valid:  
  
```  
const char *pch1 = &cch;  
const char *const pch4 = &cch;  
const char *pch5 = &ch;  
char *pch6 = &ch;  
char *const pch7 = &ch;  
const char *const pch8 = &ch;  
```  
  
 The following declaration/initializations are erroneous.  
  
```  
char *pch2 = &cch;   // Error  
char *const pch3 = &cch;   // Error  
```  
  
 The declaration of `pch2` declares a pointer through which a constant object might be modified and is therefore disallowed. The declaration of `pch3` specifies that the `pointer` is constant, not the object; the declaration is disallowed for the same reason the `pch2` declaration is disallowed.  
  
 The following eight assignments show assigning through pointer and changing of pointer value for the preceding declarations; for now, assume that the initialization was correct for `pch1` through `pch8`.  
  
```  
*pch1 = 'A';  // Error: object declared const  
pch1 = &ch;   // OK: pointer not declared const  
*pch2 = 'A';  // OK: normal pointer  
pch2 = &ch;   // OK: normal pointer  
*pch3 = 'A';  // OK: object not declared const  
pch3 = &ch;   // Error: pointer declared const  
*pch4 = 'A';  // Error: object declared const  
pch4 = &ch;   // Error: pointer declared const  
```  
  
 Pointers declared as `volatile`, or as a mixture of **const** and `volatile`, obey the same rules.  
  
 Pointers to **const** objects are often used in function declarations as follows:  
  
```  
errno_t strcpy_s( char *strDestination, size_t numberOfElements, const char *strSource );  
```  
  
 The preceding statement declares a function, [strcpy_s](../vs140/strcpy_s--wcscpy_s--_mbscpy_s.md), where two of the three arguments are of type pointer to `char`. Because the arguments are passed by reference and not by value, the function would be free to modify both `strDestination` and `strSource` if `strSource` were not declared as **const**. The declaration of `strSource` as **const** assures the caller that `strSource` cannot be changed by the called function.  
  
> [!NOTE]
>  Because there is a standard conversion from *typename* **\*** to **const** *typename* **\***, it is legal to pass an argument of type **char \*** to [strcpy_s](../vs140/strcpy_s--wcscpy_s--_mbscpy_s.md). However, the reverse is not true; no implicit conversion exists to remove the **const** attribute from an object or pointer.  
  
 A **const** pointer of a given type can be assigned to a pointer of the same type. However, a pointer that is not **const** cannot be assigned to a **const** pointer. The following code shows correct and incorrect assignments:  
  
```  
// const_pointer.cpp  
int *const cpObject = 0;  
int *pObject;  
  
int main() {  
pObject = cpObject;  
cpObject = pObject;   // C3892  
}  
```  
  
 The following sample shows how to declare an object as const if you have a pointer to a pointer to an object.  
  
```  
// const_pointer2.cpp  
struct X {  
   X(int i) : m_i(i) { }  
   int m_i;  
};  
  
int main() {  
   // correct  
   const X cx(10);  
   const X * pcx = &cx;  
   const X ** ppcx = &pcx;  
  
   // also correct  
   X const cx2(20);  
   X const * pcx2 = &cx2;  
   X const ** ppcx2 = &pcx2;  
}  
```  
  
## See Also  
 [Pointers](../vs140/Pointers--C---.md)