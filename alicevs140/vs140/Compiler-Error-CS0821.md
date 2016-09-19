---
title: "Compiler Error CS0821"
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
ms.assetid: ef449115-93e8-4fa5-848a-d30dc7f68ddf
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0821
Implicitly typed locals cannot be fixed  
  
 Implicitly typed local variables and anonymous types are not supported in the `fixed` context.  
  
### To correct this error  
  
1.  Either remove the `fixed` modifier from the variable or else give the variable an explicit type.  
  
## Example  
 The following code generates CS0821:  
  
```  
class A  
{  
    static int x;  
  
    public static int Main()  
    {  
        unsafe  
        {  
            fixed (var p = &x) { }  
        }  
        return -1;  
    }  
}  
```  
  
## See Also  
 [Implicitly Typed Local Variables (C# Programming Guide)](../vs140/Implicitly-Typed-Local-Variables--C#-Programming-Guide-.md)