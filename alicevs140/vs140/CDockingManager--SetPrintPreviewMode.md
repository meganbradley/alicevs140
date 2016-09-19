---
title: "CDockingManager::SetPrintPreviewMode"
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
ms.assetid: 8075a923-ffcb-4523-8bed-ab7e1827e85e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::SetPrintPreviewMode
Sets the print preview mode of the bars that are displayed in the print preview.  
  
## Syntax  
  
```  
void SetPrintPreviewMode(  
   BOOL bPreview,  
   CPrintPreviewState* pState  
);  
```  
  
#### Parameters  
 [in] `bPreview`  
 `TRUE` if print preview mode is set; `FALSE` otherwise.  
  
 [in] `pState`  
 A pointer to a preview state. This parameter is not used.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)