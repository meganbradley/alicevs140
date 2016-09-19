---
title: "Compiler Error CS0466"
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
ms.assetid: db6be72b-120a-4b48-b41c-a738d02adae0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0466
'method1' should not have a params parameter since 'method2' does not  
  
 You cannot use `params` parameter on a class member if the implemented interface doesn't use it.  
  
## Example  
 The following sample generates CS0466.  
  
```  
// CS0466.cs  
interface I  
{  
   void F1(params int[] a);  
   void F2(int[] a);  
}  
  
class C : I  
{  
   void I.F1(params int[] a) {}  
   void I.F2(params int[] a) {}   // CS0466  
   void I.F2(int[] a) {}   // OK  
  
   public static void Main()  
   {  
      I i = (I) new C();  
  
      i.F1(new int[] {1, 2} );  
      i.F2(new int[] {1, 2} );  
   }  
}  
```