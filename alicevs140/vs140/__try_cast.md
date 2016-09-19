---
title: "__try_cast"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9e5da3a-f5b9-4915-b30a-a432e8574d03
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# __try_cast
**Note** This topic applies only to version 1 of Managed Extensions for C++. This syntax should only be used to maintain version 1 code. See [safe_cast](../vs140/safe_cast--C---Component-Extensions-.md) for information on using the equivalent functionality in the new syntax.  
  
 Performs the specified cast or throws an exception if the cast fails.  
  
## Syntax  
  
```  
  
__try_cast <  
 type-id  
 > ( expression )  
```  
  
## Remarks  
 The `__try_cast` keyword (similar in behavior to [dynamic_cast](../vs140/dynamic_cast-Operator.md)) provides support for automatically throwing an exception (of type **System::InvalidCastException**) whenever the specified casting operation fails.  
  
 The `__try_cast` keyword can be used during the testing phase of your application, automatically alerting you to possible casting failures.  
  
 When porting Managed Extensions for C++, replace `__try_cast` calls with [safe_cast](../vs140/safe_cast--C---Component-Extensions-.md).  
  
 `__try_cast` does not work on casts of pointer to value types ([__value](../vs140/__value.md)), since it is not possible to check the types at runtime.  
  
## Example  
 In the following example, an attempt to cast a pointer (of `Derived` type) to another pointer (of `MoreDerived` type) is made. If the cast fails, it is caught and reported by the catch block:  
  
```  
// keyword__try_cast.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
using namespace System;  
  
__gc struct Base {};   
__gc struct Derived : Base {};  
__gc struct MoreDerived : Derived {};  
  
int main() {  
   Base*bp = new Derived;  
   try {  
       MoreDerived* mdp = __try_cast<MoreDerived*>(bp);  
   }  
   catch(System::InvalidCastException*) {  
       Console::WriteLine("Could not cast 'bp' to MoreDerived*");  
   }  
}  
```  
  
## Output  
  
```  
Could not cast 'bp' to MoreDerived*  
```