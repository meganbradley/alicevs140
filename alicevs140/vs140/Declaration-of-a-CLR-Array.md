---
title: "Declaration of a CLR Array"
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
ms.assetid: 36a8883c-2663-43f0-a90c-28f27035e036
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Declaration of a CLR Array
The syntax for declaring, instantiating, and initializing a managed array has changed from Managed Extensions for C++ to [!INCLUDE[cpp_current_long](../vs140/includes/cpp_current_long_md.md)].  
  
 The declaration of a CLR array object in Managed Extensions was an extension of the standard array declaration in which a `__gc` keyword was placed between the name of the array object and its possibly comma-filled dimension, as in the following pair of examples:  
  
```  
void PrintValues( Object* myArr __gc[]);  
void PrintValues( int myArr __gc[,,]);  
```  
  
 This has been simplified in the new syntax, in which we use a template-like declaration similar to the STL `vector` declaration. The first parameter indicates the element type. The second parameter specifies the array dimension (with a default value of 1, so only multiple dimensions require a second argument). The array object itself is a tracking handle, and so must be given a hat. If the element type is also a reference type, it also requires a hat. For example, the above example, when expressed in the new syntax, looks as follows:  
  
```  
void PrintValues( array<Object^>^ myArr );  
void PrintValues( array<int,3>^ myArr );  
```  
  
 Because a reference type is a tracking handle rather than an object, it is possible to specify a CLR array as the return type of a function. (In contrast, it is not possible to specify the native array as the return type of a function.) The syntax for doing this in Managed Extensions was somewhat non-intuitive. For example:  
  
```  
Int32 f() [];  
int GetArray() __gc[];  
```  
  
 In [!INCLUDE[cpp_current_long](../vs140/includes/cpp_current_long_md.md)], the declaration is much simpler. For example,  
  
```  
array<Int32>^ f();  
array<int>^ GetArray();  
```  
  
 The shorthand initialization of a local managed array is supported in both versions of the language. For example:  
  
```  
int GetArray() __gc[] {  
   int a1 __gc[] = { 1, 2, 3, 4, 5 };  
   Object* myObjArray __gc[] = {   
      __box(26), __box(27), __box(28), __box(29), __box(30)  
   };  
   return a1;  
}  
```  
  
 is considerably simplified in the new syntax (note that because boxing is implicit in the new syntax, the `__box` operator has been eliminated – see [Value Types and Their Behaviors](../vs140/Value-Types-and-Their-Behaviors--C---CLI-.md) for a discussion):  
  
```  
array<int>^ GetArray() {  
   array<int>^ a1 = {1,2,3,4,5};  
   array<Object^>^ myObjArray = {26,27,28,29,30};  
   return a1;  
}  
```  
  
 Because an array is a CLR reference type, the declaration of each array object is a tracking handle. Therefore, array objects must be allocated on the CLR heap. (The shorthand notation hides the managed heap allocation.) Here is the explicit form of an array object initialization under Managed Extensions:  
  
```  
Object* myArray[] = new Object*[2];  
String* myMat[,] = new String*[4,4];  
```  
  
 Under the new syntax, the `new` expression is replaced with `gcnew`. The dimension sizes are passed as parameters to the `gcnew` expression, as follows:  
  
```  
array<Object^>^ myArray = gcnew array<Object^>(2);  
array<String^,2>^ myMat = gcnew array<String^,2>(4,4);  
```  
  
 In the new syntax, an explicit initialization list can follow the `gcnew` expression; this was not supported in Managed Extensions. For example:  
  
```  
// explicit initialization list following gcnew   
// was not supported in Managed Extensions  
array<Object^>^ myArray =   
   gcnew array<Object^>(4){ 1, 1, 2, 3 };  
```  
  
## See Also  
 [The Managed Types](../vs140/Managed-Types--C---CL-.md)   
 [array](../vs140/Arrays--C---Component-Extensions-.md)