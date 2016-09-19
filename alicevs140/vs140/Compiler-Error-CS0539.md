---
title: "Compiler Error CS0539"
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
ms.assetid: 41b8975c-abd1-4a36-98a4-8efa5fb0502a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0539
'member' in explicit interface declaration is not a member of interface  
  
 An attempt was made to explicitly declare an [interface](../vs140/interface--C#-Reference-.md) member that does not exist. You should either delete the declaration or change it so that it refers to a valid interface member.  
  
 The following sample generates CS0539:  
  
```  
// CS0539.cs  
namespace x  
{  
   interface I  
   {  
      void m();  
   }  
  
   public class clx : I  
   {  
      void I.x()   // CS0539  
      {  
      }  
  
      public static int Main()  
      {  
         return 0;  
      }  
   }  
}  
```