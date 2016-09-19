---
title: "CMouseManager::GetViewNames"
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
ms.assetid: 06636474-b321-4fc7-907d-71b96c676d31
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMouseManager::GetViewNames
Retrieves a list of all the registered view names.  
  
## Syntax  
  
```  
void GetViewNames(  
   CStringList& listOfNames   
) const;  
```  
  
#### Parameters  
 [out] `listOfNames`  
 A reference to `CStringList` object.  
  
## Remarks  
 This method fills the parameter `listOfNames` with the names of all the views registered by using [CMouseManager::AddView](../vs140/CMouseManager--AddView.md).  
  
## Requirements  
 **Header:** afxmousemanager.h  
  
## See Also  
 [CMouseManager Class](../vs140/CMouseManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMouseManager::AddView](../vs140/CMouseManager--AddView.md)