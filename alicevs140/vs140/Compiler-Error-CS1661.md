---
title: "Compiler Error CS1661"
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
ms.assetid: 162d5736-ca3c-4a09-a5d9-a19da3d5bf24
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1661
Cannot convert anonymous method block to delegate type 'delegate type' because the specified block's parameter types do not match the delegate parameter types  
  
 This error occurs if, in an anonymous method definition, the parameter types of the anonymous method do not match the delegate parameter types. Check the number of parameters, the parameter types, and any ref or out parameters and verify an exact match.  
  
 The following sample generates CS1661:  
  
```  
// CS1661.cs  
  
delegate void MyDelegate(int i);  
  
class C  
{  
    public static void Main()  
    {  
        MyDelegate d = delegate(string s) { };  // CS1661  
    }  
}  
```