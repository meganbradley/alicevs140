---
title: "CComSingleThreadModel::Decrement"
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
ms.topic: reference
ms.assetid: 23fb1c95-b232-43d6-93bf-b82925b41581
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSingleThreadModel::Decrement
This static function decrements the value of the variable pointed to by `p`.  
  
## Syntax  
  
```  
  
      static ULONG WINAPI Decrement(  
   LPLONG p   
) throw();  
```  
  
#### Parameters  
 `p`  
 [in] Pointer to the variable to be decremented.  
  
## Return Value  
 The result of the decrement.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComSingleThreadModel Class](../vs140/CComSingleThreadModel-Class.md)   
 [CComSingleThreadModel::Increment](../vs140/CComSingleThreadModel--Increment.md)