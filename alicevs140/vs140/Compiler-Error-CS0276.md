---
title: "Compiler Error CS0276"
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
ms.assetid: 0c49017f-c7a9-42a5-9d0a-6f1d82142bd7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0276
'property/indexer': accessibility modifiers on accessors may only be used if the property or indexer has both a get and a set accessor  
  
 This error occurs when you declare a property or indexer with one accessor only, and use an access modifier on the accessor. To resolve, remove the access modifier or add another accessor.  
  
## Example  
 The following example generates CS0276:  
  
```  
// CS0276.cs  
public class MyClass  
{  
    public int Property  
    {  
        protected set { }   // CS0276  
    }  
    public int Property2  
    {  
        internal get { }   // CS0276  
    }  
}  
```