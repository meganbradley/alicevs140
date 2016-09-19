---
title: "Compiler Error CS0275"
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
ms.assetid: 4d59f11c-b0ea-4c91-b2cb-cbe3be9a9ba2
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0275
'accessor': accessibility modifiers may not be used on accessors in an interface  
  
 This error occurs when you use an access modifier on any one of the accessors of a property or indexer in an interface. To resolve, remove the access modifier.  
  
## Example  
 The following example generates CS0275:  
  
```  
// CS0275.cs  
public interface MyInterface  
{  
    int Property  
    {  
        get;  
        internal set;   // CS0275  
    }  
}  
```