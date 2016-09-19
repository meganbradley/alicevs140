---
title: "CMouseManager::GetViewIconId"
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
ms.assetid: a2aafb89-ee87-4d08-833b-8c1b2ba7c283
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMouseManager::GetViewIconId
Retrieves the icon associated with a view ID.  
  
## Syntax  
  
```  
UINT GetViewIconId(  
   int iViewId   
) const;  
```  
  
#### Parameters  
 [in] `iViewId`  
 The view ID.  
  
## Return Value  
 An icon resource identifier if successful; otherwise 0.  
  
## Remarks  
 This method will fail if the view is not first registered by using [CMouseManager::AddView](../vs140/CMouseManager--AddView.md).  
  
## Requirements  
 **Header:** afxmousemanager.h  
  
## See Also  
 [CMouseManager Class](../vs140/CMouseManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMouseManager::AddView](../vs140/CMouseManager--AddView.md)