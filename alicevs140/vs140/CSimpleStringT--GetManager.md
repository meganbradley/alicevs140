---
title: "CSimpleStringT::GetManager"
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
ms.assetid: 3348dcf2-fd92-4838-a15b-474e136880a4
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::GetManager
Retrieves the memory manager of the `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
IAtlStringMgr* GetManager( ) const throw( );  
  
```  
  
## Return Value  
 A pointer to the memory manager for the `CSimpleStringT` object.  
  
## Remarks  
 Call this method to retrieve the memory manager used by the `CSimpleStringT` object. For more information on memory managers and string objects, see [Memory Management and CStringT](../vs140/Memory-Management-with-CStringT.md).  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::SetManager](../vs140/CSimpleStringT--SetManager.md)