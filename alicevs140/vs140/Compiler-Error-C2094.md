---
title: "Compiler Error C2094"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9e4f8f88-f189-46e7-91c9-481bacc7af87
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2094
label 'identifier' was undefined  
  
 The label used by a [goto](../vs140/goto--C#-Reference-.md) statement does not exist in the function.  
  
 The following sample generates C2094:  
  
```  
// C2094.c  
int main() {  
   goto test;  
}   // C2094  
```  
  
 Possible resolution:  
  
```  
// C2094b.c  
int main() {  
   goto test;  
   test:   
   {  
   }  
}  
```