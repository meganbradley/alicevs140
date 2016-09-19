---
title: "Managed Types and the main Function (C++-CLI)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
H1: Managed Types and the main Function (C++/CLI)
ms.assetid: 9d0e9620-58c4-4dac-a0e1-ffeb95f80fa5
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Managed Types and the main Function (C++-CLI)
When writing an application using **/clr**, the arguments of the **main()** function cannot be of a managed type.  
  
 An example of a proper signature is:  
  
```  
// managed_types_and_main.cpp  
// compile with: /clr  
int main(int, char*[], char*[]) {}  
```  
  
## See Also  
 [Managed Types (C++/CLI)](../vs140/Managed-Types--C---CLI-.md)