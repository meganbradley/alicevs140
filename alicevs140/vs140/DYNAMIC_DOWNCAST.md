---
title: "DYNAMIC_DOWNCAST"
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
ms.assetid: 1d77f9a6-e187-46d5-954c-2a6af8bf6b03
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DYNAMIC_DOWNCAST
Provides a handy way to cast a pointer to a pointer to a class object while checking to see if the cast is legal.  
  
## Syntax  
  
```  
  
DYNAMIC_DOWNCAST(  
class  
,   
pointer )  
```  
  
#### Parameters  
 `class`  
 The name of a class.  
  
 `pointer`  
 A pointer to be cast to a pointer to an object of type `class`.  
  
## Remarks  
 The macro will cast the `pointer` parameter to a pointer to an object of the `class` parameter's type.  
  
 If the object referenced by the pointer is a "kind of" the identified class, the macro returns the appropriate pointer. If it is not a legal cast, the macro returns **NULL**.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [STATIC_DOWNCAST](../vs140/STATIC_DOWNCAST.md)   
 [dynamic_cast Operator](../vs140/dynamic_cast-Operator.md)