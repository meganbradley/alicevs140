---
title: "CMFCVisualManager::GetInstance"
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
ms.assetid: b77e6cb7-bf84-47ef-9c38-8b8eb993dda2
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::GetInstance
Returns a pointer to the current [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md) object for the application.  
  
## Syntax  
  
```  
static CMFCVisualManager* GetInstance();  
```  
  
## Return Value  
 A pointer to a `CMFCVisualManager` object.  
  
## Remarks  
 An application can only have one `CMFCVisualManager` object associated with it. This includes any object derived from the `CMFCVisualManager` class. This method returns a pointer to the associated `CMFCVisualManager` object. If the application does not have an associated `CMFCVisualManager` object, this method will create one and associate it with the application.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)