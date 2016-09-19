---
title: "CMFCVisualManager::AlwaysHighlight3DTabs"
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
ms.assetid: fac92223-d63e-43db-aece-a3ba0da30480
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::AlwaysHighlight3DTabs
The framework calls this method to determine whether 3D tabs should always be highlighted in the application.  
  
## Syntax  
  
```  
virtual BOOL AlwaysHighlight3DTabs() const;  
```  
  
## Return Value  
 `TRUE` if 3D tabs should be highlighted.  
  
## Remarks  
 Override this function in a derived visual manager and return `TRUE` if 3D tabs should always be highlighted. The default implementation of this method returns `FALSE`.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)