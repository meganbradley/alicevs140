---
title: "Compiler Error CS0274"
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
ms.assetid: bbd2d64e-a756-4713-b9ed-711d50b65e00
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0274
Cannot specify accessibility modifiers for both accessors of the property or indexer 'property/indexer'  
  
 This error occurs when you declare a property or indexer with access modifiers on both its accessors. To resolve this error, use an access modifier on only one of the two accessors. For more information, see [Accessor Accessibility](../vs140/Restricting-Accessor-Accessibility--C#-Programming-Guide-.md).  
  
 The following example generates CS0274:  
  
```  
// CS0274.cs  
public class MyClass  
{  
    public int Property   // CS0274  
    {  
        public get { return 0; }  
        protected set { }  
    }  
}  
```