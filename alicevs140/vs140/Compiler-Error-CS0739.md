---
title: "Compiler Error CS0739"
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
ms.assetid: c2a83015-401c-4d85-bb19-ed29800904c1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0739
'type name' duplicate TypeForwardedToAttribute.  
  
 An assembly can have no more than one <xref:System.Runtime.CompilerServices.TypeForwardedToAttribute?qualifyHint=False> to an external type.  
  
### To correct this error  
  
1.  Locate and remove the duplicate <xref:System.Runtime.CompilerServices.TypeForwardedToAttribute?qualifyHint=False>.  
  
## Example  
 The following code generates CS0739:  
  
```  
// CS0739.cs  
// CS0739  
// Assume that a class Test is declared in a separate dll  
// with a namespace that is named cs739dll.  
[assembly: System.Runtime.CompilerServices.TypeForwardedTo(typeof(cs739dll.Test))]  
[assembly: System.Runtime.CompilerServices.TypeForwardedTo(typeof(cs739dll.Test))]  
namespace cs0739  
{  
    class Program  
    {  
        static void Main(string[] args)  
        {  
        }  
    }  
}  
```  
  
## See Also  
 <xref:System.Runtime.CompilerServices.TypeForwardedToAttribute?qualifyHint=False>