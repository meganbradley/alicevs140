---
title: "CWinApp::DelRegTree"
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
ms.assetid: 60745561-388a-4976-a519-4762590e196d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::DelRegTree
Deletes a specific registry key and all its subkeys.  
  
## Syntax  
  
```  
  
      LONG DelRegTree(  
   HKEY hParentKey,  
   const CString& strKeyName  
);  
LONG DelRegTree(  
   HKEY hParentKey,  
   const CString& strKeyName,  
   CAtlTransactionManager* pTM = NULL  
);  
```  
  
#### Parameters  
 *hParentKey*  
 Handle to a registry key.  
  
 *strKeyName*  
 The name of the registry key to be deleted.  
  
 *pTM*  
 Pointer to CAtlTransactionManager object.  
  
## Return Value  
 If the function succeeds, the return value is ERROR_SUCCESS. If the function fails, the return value is a nonzero error code defined in Winerror.h.  
  
## Remarks  
 Call this function to delete the specified key and its subkeys.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)