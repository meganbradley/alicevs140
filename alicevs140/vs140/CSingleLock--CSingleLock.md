---
title: "CSingleLock::CSingleLock"
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
ms.assetid: a3f9f9d4-d508-4080-8f90-d930f7cb7b72
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSingleLock::CSingleLock
Constructs a `CSingleLock` object.  
  
## Syntax  
  
```  
  
      explicit CSingleLock(  
   CSyncObject* pObject,  
   BOOL bInitialLock = FALSE   
);  
```  
  
#### Parameters  
 `pObject`  
 Points to the synchronization object to be accessed. Cannot be **NULL**.  
  
 `bInitialLock`  
 Specifies whether to initially attempt to access the supplied object.  
  
## Remarks  
 This function is generally called from within an access member function of the controlled resource.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#19)]  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CSingleLock Class](../vs140/CSingleLock-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)