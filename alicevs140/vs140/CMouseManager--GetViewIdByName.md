---
title: "CMouseManager::GetViewIdByName"
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
ms.assetid: 45f7cb80-ad5f-4890-881e-784b8b9db449
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMouseManager::GetViewIdByName
Retrieves the view ID associated with a view name.  
  
## Syntax  
  
```  
int GetViewIdByName(  
   LPCTSTR lpszName   
) const;  
```  
  
#### Parameters  
 [in] `lpszName`  
 The view name.  
  
## Return Value  
 A view ID if successful; otherwise 0.  
  
## Remarks  
 This method searches through views registered by using [CMouseManager::AddView](../vs140/CMouseManager--AddView.md).  
  
## Requirements  
 **Header:** afxmousemanager.h  
  
## See Also  
 [CMouseManager Class](../vs140/CMouseManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)