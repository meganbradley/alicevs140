---
title: "Compiler Error CS1632"
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
ms.assetid: fa18061a-8c6c-4788-b74e-62bacb16aed8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1632
Control cannot leave the body of an anonymous method or lambda expression  
  
 This error occurs if a jump statement (**break**, `goto`, **continue**, etc.) attempts to move control out of an anonymous method block. An anonymous method block is a function body and can only be exited by a return statement or by reaching the end of the block.  
  
 The following sample generates CS1632:  
  
```  
// CS1632.cs  
// compile with: /target:library  
delegate void MyDelegate();  
class MyClass  
{  
   public void Test()  
   {        
      for (int i = 0 ; i < 5 ; i++)  
      {  
         MyDelegate d = delegate {  
            break;   // CS1632  
          };          
      }  
   }  
}  
```