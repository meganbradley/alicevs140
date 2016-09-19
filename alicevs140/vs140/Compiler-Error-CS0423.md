---
title: "Compiler Error CS0423"
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
ms.assetid: e4ec44b6-bf9c-41f7-a309-8f8b9e325691
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0423
Since 'class' has the ComImport attribute, 'method' must be extern or abstract  
  
 Specifying the ComImport attribute implies that the implementation for the class is to be imported from a COM module. Additional methods may not be defined.  
  
 The following sample generates CS0423:  
  
```  
// CS0423.cs  
  
using System.Runtime.InteropServices;  
  
[  
  ComImport,  
  Guid("7ab770c7-0e23-4d7a-8aa2-19bfad479829")  
]  
class ImageProperties  
{  
  public static void Main()  // CS0423  
  {  
    ImageProperties i = new ImageProperties();  
  }  
}  
```