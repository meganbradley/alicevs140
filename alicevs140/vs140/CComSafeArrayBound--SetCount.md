---
title: "CComSafeArrayBound::SetCount"
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
ms.assetid: 789c9b64-863a-47af-9a32-2a8792615a09
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArrayBound::SetCount
Call this method to set the number of elements.  
  
## Syntax  
  
```  
  
      ULONG SetCount(  
   ULONG ulCount   
) throw( );  
```  
  
#### Parameters  
 `ulCount`  
 The number of elements.  
  
## Return Value  
 Returns the number of elements in the `CComSafeArrayBound` object.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArrayBound Class](../vs140/CComSafeArrayBound-Class.md)   
 [CComSafeArrayBound::GetCount](../vs140/CComSafeArrayBound--GetCount.md)   
 [CComSafeArrayBound::SetLowerBound](../vs140/CComSafeArrayBound--SetLowerBound.md)