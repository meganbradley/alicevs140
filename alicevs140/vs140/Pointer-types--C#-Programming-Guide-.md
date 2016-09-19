---
title: "Pointer types (C# Programming Guide)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3319faf9-336d-4148-9af2-1da2579cdd1e
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Pointer types (C# Programming Guide)
In an unsafe context, a type may be a pointer type, a value type, or a reference type. A pointer type declaration takes one of the following forms:  
  
```  
type* identifier;  
void* identifier; //allowed but not recommended  
```  
  
 Any of the following types may be a pointer type:  
  
-   [sbyte](../Topic/sbyte%20\(C%23%20Reference\).md), [byte](../Topic/byte%20\(C%23%20Reference\).md), [short](../Topic/short%20\(C%23%20Reference\).md), [ushort](../Topic/ushort%20\(C%23%20Reference\).md), [int](../Topic/int%20\(C%23%20Reference\).md), [uint](../Topic/uint%20\(C%23%20Reference\).md), [long](../vs140/long--C#-Reference-.md), [ulong](../Topic/ulong%20\(C%23%20Reference\).md), [char](../vs140/char--C#-Reference-.md), [float](../vs140/float--C#-Reference-.md), [double](../vs140/double--C#-Reference-.md), [decimal](../Topic/decimal%20\(C%23%20Reference\).md), or [bool](../Topic/bool%20\(C%23%20Reference\).md).  
  
-   Any [enum](../Topic/enum%20\(C%23%20Reference\).md) type.  
  
-   Any pointer type.  
  
-   Any user-defined struct type that contains fields of unmanaged types only.  
  
 Pointer types do not inherit from [object](../vs140/object--C#-Reference-.md) and no conversions exist between pointer types and `object`. Also, boxing and unboxing do not support pointers. However, you can convert between different pointer types and between pointer types and integral types.  
  
 When you declare multiple pointers in the same declaration, the asterisk (*) is written together with the underlying type only; it is not used as a prefix to each pointer name. For example:  
  
```  
int* p1, p2, p3;   // Ok  
int *p1, *p2, *p3;   // Invalid in C#  
```  
  
 A pointer cannot point to a reference or to a [struct](../vs140/struct--C#-Reference-.md) that contains references, because an object reference can be garbage collected even if a pointer is pointing to it. The garbage collector does not keep track of whether an object is being pointed to by any pointer types.  
  
 The value of the pointer variable of type `myType*` is the address of a variable of type `myType`. The following are examples of pointer type declarations:  
  
|Example|Description|  
|-------------|-----------------|  
|`int* p`|`p` is a pointer to an integer.|  
|`int** p`|`p` is a pointer to a pointer to an integer.|  
|`int*[] p`|`p` is a single-dimensional array of pointers to integers.|  
|`char* p`|`p` is a pointer to a char.|  
|`void* p`|`p` is a pointer to an unknown type.|  
  
 The pointer indirection operator * can be used to access the contents at the location pointed to by the pointer variable. For example, consider the following declaration:  
  
```  
int* myVariable;  
```  
  
 The expression `*myVariable` denotes the `int` variable found at the address contained in `myVariable`.  
  
 There are several examples of pointers in the topics [fixed Statement](../vs140/fixed-Statement--C#-Reference-.md) and [Pointer Conversions](../vs140/Pointer-Conversions--C#-Programming-Guide-.md).  The following example shows the need for the `unsafe` keyword and the `fixed` statement, and how to increment an interior pointer.  You can paste this code into the Main function of a console application to run it. (Remember to enable unsafe code in the **Project Designer**; choose **Project**, **Properties** on the menu bar, and then select **Allow unsafe code** in the **Build** tab.)  
  
```  
// Normal pointer to an object.  
int[] a = new int[5] {10, 20, 30, 40, 50};  
// Must be in unsafe code to use interior pointers.  
unsafe  
{  
    // Must pin object on heap so that it doesn't move while using interior pointers.  
    fixed (int* p = &a[0])  
    {  
        // p is pinned as well as object, so create another pointer to show incrementing it.  
        int* p2 = p;  
        Console.WriteLine(*p2);  
        // Incrementing p2 bumps the pointer by four bytes due to its type ...  
        p2 += 1;  
        Console.WriteLine(*p2);  
        p2 += 1;  
        Console.WriteLine(*p2);  
        Console.WriteLine("--------");  
        Console.WriteLine(*p);  
        // Deferencing p and incrementing changes the value of a[0] ...  
        *p += 1;  
        Console.WriteLine(*p);  
        *p += 1;  
        Console.WriteLine(*p);  
    }  
}  
  
Console.WriteLine("--------");  
Console.WriteLine(a[0]);  
Console.ReadLine();  
  
// Output:  
//10  
//20  
//30  
//--------  
//10  
//11  
//12  
//--------  
//12  
  
```  
  
 You cannot apply the indirection operator to a pointer of type `void*`. However, you can use a cast to convert a void pointer to any other pointer type, and vice versa.  
  
 A pointer can be `null`. Applying the indirection operator to a null pointer causes an implementation-defined behavior.  
  
 Be aware that passing pointers between methods can cause undefined behavior. Examples are returning a pointer to a local variable through an Out or Ref parameter or as the function result. If the pointer was set in a fixed block, the variable to which it points may no longer be fixed.  
  
 The following table lists the operators and statements that can operate on pointers in an unsafe context:  
  
|Operator/Statement|Use|  
|-------------------------|---------|  
|*|Performs pointer indirection.|  
|->|Accesses a member of a struct through a pointer.|  
|[]|Indexes a pointer.|  
|`&`|Obtains the address of a variable.|  
|++ and --|Increments and decrements pointers.|  
|+ and -|Performs pointer arithmetic.|  
|==, !=, <, >, <=, and >=|Compares pointers.|  
|`stackalloc`|Allocates memory on the stack.|  
|`fixed` statement|Temporarily fixes a variable so that its address may be found.|  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Unsafe Code and Pointers (C#)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md)   
 [Pointer Conversions](../vs140/Pointer-Conversions--C#-Programming-Guide-.md)   
 [Pointer Expressions](../vs140/Pointer-Expressions--C#-Programming-Guide-.md)   
 [Types](../vs140/Types--C#-Reference-.md)   
 [unsafe](../vs140/unsafe--C#-Reference-.md)   
 [fixed Statement](../vs140/fixed-Statement--C#-Reference-.md)   
 [stackalloc](../vs140/stackalloc--C#-Reference-.md)   
 [Boxing and Unboxing (C# Programming Guide)](../Topic/Boxing%20and%20Unboxing%20\(C%23%20Programming%20Guide\).md)