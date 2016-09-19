---
title: "CSingleLock::IsLocked"
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
ms.assetid: 9d23fecc-be98-4fa1-a878-667b7178f9e3
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSingleLock::IsLocked
Determines if the object associated with the `CSingleLock` object is nonsignaled (unavailable).  
  
## Syntax  
  
```  
  
BOOL IsLocked( );  
  
```  
  
## Return Value  
 Nonzero if the object is locked; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#20)]  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CSingleLock Class](../vs140/CSingleLock-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)