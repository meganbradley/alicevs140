---
title: "Compiler Error CS0415"
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
ms.assetid: 1ed45b02-4568-4af4-b2a6-c8b01230d19a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0415
The 'IndexerName' attribute is valid only on an indexer that is not an explicit interface member declaration  
  
 This error occurs if you use an IndexerName attribute on an indexer that was an explicit implementation of an interface. This error may be avoided by removing the interface name from the declaration of the indexer, if possible. For more information, see the [IndexerNameAttribute Class](frlrfSystemRuntimeCompilerServicesIndexerNameAttributeClassTopic).  
  
 The following sample generates CS0415:  
  
```  
// CS0415.cs  
using System;  
using System.Runtime.CompilerServices;  
  
public interface IA  
{  
    int this[int index]  
    {  
        get;  
        set;  
    }  
}  
  
public class A : IA  
{  
    [IndexerName("Item")]  // CS0415  
    int IA.this[int index]  
    // Try this line instead:  
    // public int this[int index]  
    {  
        get { return 0; }  
        set { }  
    }  
  
    static void Main()  
    {  
    }  
}  
```