---
title: "Compiler Warning (level 2) CS1710"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 03c66a8d-30fc-4387-87f6-de759ec7ee88
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS1710
XML comment on 'type' has a duplicate typeparam tag for 'parameter'  
  
 The documentation of a generic type includes a duplicate tag for the type parameter.  
  
## Example  
 The following code will cause warning CS1710 to appear.  
  
```  
// CS1710.cs  
// compile with: /doc:cs1710.xml  
// To resolve this warning, delete one of the duplicate <typeparam>'s.  
using System;  
class Stack<ItemType>  
{  
}  
  
/// <typeparam name="MyType">can be an int</typeparam>  
/// <typeparam name="MyType">can be an int</typeparam>  
class MyStackWrapper<MyType>  
{  
    // Open constructed type Stack<MyType>.  
    Stack<MyType> stack;  
    public MyStackWrapper(Stack<MyType> s)  
    {  
        stack = s;  
    }  
}  
  
class CMain  
{  
    public static void Main()  
    {  
        // Closed constructed type Stack<int>.  
        Stack<int> stackInt = new Stack<int>();  
        MyStackWrapper<int> MyStackWrapperInt =  
            new MyStackWrapper<int>(stackInt);  
    }  
}  
```