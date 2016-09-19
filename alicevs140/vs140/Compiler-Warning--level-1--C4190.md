---
title: "Compiler Warning (level 1) C4190"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: a4d0ad93-a19a-4063-addd-36d605831567
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4190
'identifier1' has C-linkage specified, but returns UDT 'identifier2' which is incompatible with C  
  
 A function or pointer to function has a UDT (user-defined type, which is a class, structure, enum, union, or [__value](../vs140/__value.md) type) as return type and `extern` "C" linkage. This is legal if:  
  
-   All calls to this function occur from C++.  
  
-   The definition of the function is in C++.  
  
## Example  
  
```  
// C4190.cpp  
// compile with: /W1 /LD  
struct X  
{  
   int i;  
   X ();  
   virtual ~X ();  
};  
  
extern "C" X func ();   // C4190  
```