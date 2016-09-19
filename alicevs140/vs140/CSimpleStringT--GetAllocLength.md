---
title: "CSimpleStringT::GetAllocLength"
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
ms.assetid: d339eb03-48f6-47e7-94bf-f3d1d5b55655
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::GetAllocLength
Retrieves the allocated length of a `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
int GetAllocLength( ) const throw( );  
  
```  
  
## Return Value  
 The number of characters allocated for this object.  
  
## Remarks  
 Call this method to determine the number of characters allocated for this `CSimpleStringT` object. See [FreeExtra](../vs140/CSimpleStringT--FreeExtra.md) for an example of calling this function.  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)