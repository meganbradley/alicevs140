---
title: "Compiler Error C2048"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 44704726-85fc-42f0-afb9-194df8c4ca7c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2048
more than one default  
  
 A `switch` statement contains multiple `default` labels. Delete one of the `default` labels to resolve the error.  
  
 The following sample generates C2048:  
  
```  
// C2048.cpp  
int main() {  
   int a = 1;  
   switch (a) {  
      case 1:  
         a = 0;  
      default:  
         a = 2;  
      default:   // C2048  
         a = 3;  
   }  
}  
```  
  
 Possible resolution:  
  
```  
// C2048b.cpp  
int main() {  
   int a = 1;  
   switch (a) {  
      case 1:  
         a = 0;  
      default:  
         a = 2;  
   }  
}  
```