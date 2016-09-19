---
title: "CSingleLock::Unlock"
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
ms.assetid: 91354207-3458-416e-96da-c21e5d6b656a
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSingleLock::Unlock
Releases the synchronization object owned by `CSingleLock`.  
  
## Syntax  
  
```  
  
      BOOL Unlock( );   
BOOL Unlock(  
   LONG lCount,  
   LPLONG lPrevCount = NULL   
);  
```  
  
#### Parameters  
 `lCount`  
 Number of accesses to release. Must be greater than 0. If the specified amount would cause the object's count to exceed its maximum, the count is not changed and the function returns **FALSE**.  
  
 `lPrevCount`  
 Points to a variable to receive the previous count of the synchronization object. If **NULL**, the previous count is not returned.  
  
## Return Value  
 Nonzero if the function was successful; otherwise 0.  
  
## Remarks  
 This function is called by `CSingleLock`'s destructor.  
  
 If you need to release more than one access count of a semaphore, use the second form of `Unlock` and specify the number of accesses to release.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#21)]  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CSingleLock Class](../vs140/CSingleLock-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)