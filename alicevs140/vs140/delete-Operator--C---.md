---
title: "delete Operator (C++)"
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
ms.assetid: de39c900-3f57-489c-9598-dcb73c4b3930
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# delete Operator (C++)
Deallocates a block of memory.  
  
## Syntax  
  
```  
[::] delete cast-expression  
[::] delete [ ] cast-expression  
```  
  
## Remarks  
 The *cast-expression* argument must be a pointer to a block of memory previously allocated for an object created with the [new operator](../vs140/new-Operator--C---.md). The **delete** operator has a result of type `void` and therefore does not return a value. For example:  
  
```  
CDialog* MyDialog = new CDialog;  
// use MyDialog  
delete MyDialog;  
```  
  
 Using **delete** on a pointer to an object not allocated with **new** gives unpredictable results. You can, however, use **delete** on a pointer with the value 0. This provision means that, when **new** returns 0 on failure, deleting the result of a failed **new** operation is harmless. See [The new and delete Operators](../vs140/new-and-delete-Operators.md) for more information.  
  
 The **new** and **delete** operators can also be used for built-in types, including arrays. If `pointer` refers to an array, place empty brackets before `pointer`:  
  
```  
int* set = new int[100];  
//use set[]  
delete [] set;  
```  
  
 Using the **delete** operator on an object deallocates its memory. A program that dereferences a pointer after the object is deleted can have unpredictable results or crash.  
  
 When **delete** is used to deallocate memory for a C++ class object, the object's destructor is called before the object's memory is deallocated (if the object has a destructor).  
  
 If the operand to the **delete** operator is a modifiable l-value, its value is undefined after the object is deleted.  
  
## Using delete  
 There are two syntactic variants for the [delete operator](../vs140/delete-Operator--C---.md): one for single objects and the other for arrays of objects. The following code fragment shows how these differ:  
  
```  
// expre_Using_delete.cpp  
struct UDType   
{  
};  
  
int main()  
{  
   // Allocate a user-defined object, UDObject, and an object  
   //  of type double on the free store using the  
   //  new operator.  
   UDType *UDObject = new UDType;  
   double *dObject = new double;  
   // Delete the two objects.  
   delete UDObject;  
   delete dObject;   
   // Allocate an array of user-defined objects on the  
   // free store using the new operator.  
   UDType (*UDArr)[7] = new UDType[5][7];  
   // Use the array syntax to delete the array of objects.  
   delete [] UDArr;  
}  
```  
  
 The following two cases produce undefined results: using the array form of delete (delete [ ]) on an object and using the nonarray form of delete on an array.  
  
## Example  
 For examples of using **delete**, see [new operator](../vs140/new-Operator--C---.md).  
  
## How delete works  
 The [delete operator](../vs140/delete-Operator--C---.md) invokes the function [operator delete](../vs140/operator-delete-Function.md).  
  
 For objects not of class type ([class](../vs140/class--C---.md), [struct](../vs140/struct--C---.md), or [union](../vs140/Unions.md)), the global delete operator is invoked. For objects of class type, the name of the deallocation function is resolved in global scope if the delete expression begins with the unary scope resolution operator (::). Otherwise, the delete operator invokes the destructor for an object prior to deallocating memory (if the pointer is not null). The delete operator can be defined on a per-class basis; if there is no such definition for a given class, the global operator delete is invoked. If the delete expression is used to deallocate a class object whose static type has a virtual destructor, the deallocation function is resolved through the virtual destructor of the dynamic type of the object.  
  
## See Also  
 [Expressions with Unary Operators](../vs140/Expressions-with-Unary-Operators.md)   
 [Keywords](../vs140/Keywords--C---.md)   
 [new and delete Operators](../vs140/new-and-delete-Operators.md)   
 [operator delete Function](../vs140/operator-delete-Function.md)