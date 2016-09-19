---
title: "CConnectionPoint::GetNextConnection"
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
ms.assetid: 16c2bc3f-5b8a-405b-857f-d2c50055ac9d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CConnectionPoint::GetNextConnection
Retrieves a pointer to the connection element at `pos`.  
  
## Syntax  
  
```  
  
      LPUNKNOWN GetNextConnection(  
   POSITION& pos  
) const;  
```  
  
#### Parameters  
 `pos`  
 Specifies a reference to a **POSITION** value returned by a previous `GetNextConnection` or [GetStartPosition](../vs140/CConnectionPoint--GetStartPosition.md) call.  
  
## Return Value  
 A pointer to the connection element specified by `pos`, or NULL.  
  
## Remarks  
 This function is most useful for iterating through all the elements in the connection map. When iterating, skip any NULLs returned from this function.  
  
## Example  
 [!CODE [NVC_MFCConnectionPoints#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCConnectionPoints#4)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [CConnectionPoint Class](../vs140/CConnectionPoint-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)