---
title: "CMFCRibbonPanel::GetPreferedMenuLocation"
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
ms.assetid: efb77cf0-0b26-4189-b7cb-0e528108202c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::GetPreferedMenuLocation
Retrieves the preferred display rectangle for the pop-up menu of the ribbon panel.  
  
## Syntax  
  
```  
virtual BOOL GetPreferedMenuLocation(  
    CRect& rect  
);  
```  
  
#### Parameters  
 [out] `rect`  
 This parameter is not used.  
  
## Return Value  
 Always returns `FALSE`.  
  
## Remarks  
 This method always returns `FALSE`. Override this method to retrieve the preferred display rectangle for the pop-up menu of the ribbon panel.  
  
## Requirements  
 **Header:** afxribbonpanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)