---
title: "IAtlStringMgr::Clone"
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
ms.assetid: ba3af525-ce89-4490-84a3-0ee54a1c6c25
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAtlStringMgr::Clone
Returns a pointer to a new string manager for use with another instance of `CSimpleStringT`.  
  
## Syntax  
  
```  
  
IAtlStringMgr* Clone( ) throw( );  
  
```  
  
## Return Value  
 Returns a copy of the `IAtlStringMgr` object.  
  
## Remarks  
 Commonly called by the framework when a string manager is needed for a new string. In most cases, the **this** pointer is returned.  
  
 However, if the memory manager does not support being used by multiple instances of `CSimpleStringT`, a pointer to a sharable string manager should be returned.  
  
> [!NOTE]
>  For usage examples, see [Memory Management and CStringT](../vs140/Memory-Management-with-CStringT.md).  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [IAtlStringMgr Class](../vs140/IAtlStringMgr-Class.md)