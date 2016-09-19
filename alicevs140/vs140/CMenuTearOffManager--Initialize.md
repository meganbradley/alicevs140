---
title: "CMenuTearOffManager::Initialize"
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
ms.assetid: f3cabcb3-24c1-49ad-8f13-b4a5ee82d15f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenuTearOffManager::Initialize
Initializes a [CMenuTearOffManager](../vs140/CMenuTearOffManager-Class.md) object.  
  
## Syntax  
  
```  
BOOL Initialize(  
   LPCTSTR lpszRegEntry,  
   UINT uiTearOffMenuFirst,  
   UINT uiTearOffMenuLast  
);  
```  
  
#### Parameters  
 [in] `lpszRegEntry`  
 A string that contains the path of a registry entry. Your applications stores the settings for tear-off bars in this registry entry.  
  
 [in] `uiTearOffMenuFirst`  
 The first menu ID for a tear-off menu.  
  
 [in] `uiTearOffMenuLast`  
 The last menu ID for a tear-off menu.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The range of menu IDs from `uiTearOffMenuFirst` to `uiTearOffMenuLast` must be a continuous interval. The interval defines the number of tear-off menus that can appear at the same time in the application.  
  
## Requirements  
 **Header:** afxmenutearoffmanager.h  
  
## See Also  
 [CMenuTearOffManager Class](../vs140/CMenuTearOffManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)