---
title: "Compiler Error C2063"
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
ms.assetid: 0a90c18f-4029-416a-9128-e8713b53e6f1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2063
'identifier' : not a function  
  
 The identifier is used as a function but not declared as a function.  
  
 The following sample generates C2063:  
  
```  
// C2063.c  
int main() {  
   int i, j;  
   j = i();    // C2063, i is not a function  
}  
```  
  
 Possible resolution:  
  
```  
// C2063b.c  
int i() { return 0;}  
int main() {  
   int j;  
   j = i();  
}  
```