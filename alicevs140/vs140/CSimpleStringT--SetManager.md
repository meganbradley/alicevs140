---
title: "CSimpleStringT::SetManager"
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
ms.assetid: c3042934-59d3-4485-bf1c-16fbf36f37e2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::SetManager
Specifies the memory manager of the `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
      void SetManager(  
   IAtlStringMgr* pStringMgr  
);  
```  
  
#### Parameters  
 `pStringMgr`  
 A pointer to the new memory manager.  
  
## Remarks  
 Call this method to specify a new memory manager used by the `CSimpleStringT` object. For more information on memory managers and string objects, see [Memory Management and CStringT](../vs140/Memory-Management-with-CStringT.md).  
  
## Example  
 The following example demonstrates the use of `CSimpleStringT::SetManager`.  
  
 [!CODE [NVC_ATLMFC_Utilities#89](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#89)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::GetManager](../vs140/CSimpleStringT--GetManager.md)