---
title: "Compiler Error CS0407"
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
ms.assetid: 59112fb9-4641-466e-b738-b3228539a09e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0407
'return-type method' has the wrong return type  
  
 The method was not compatible with the delegate type. The argument types matched, but the return type was not the correct return type for that delegate. To avoid this error, use a different method, change the method's return type, or change the delegate's return type.  
  
## Example  
 The following sample generates CS0407:  
  
```  
// CS0407.cs  
public delegate int MyDelegate();  
  
class C  
{  
    MyDelegate d;  
  
    public C()  
    {  
        d = new MyDelegate(F);  // OK: F returns int  
        d = new MyDelegate(G);  // CS0407 – G doesn't return int  
    }  
  
    public int F()  
    {  
        return 1;  
    }  
  
    public void G()  
    {  
    }  
  
    public static void Main()  
    {  
        C c1 = new C();  
    }  
}  
```