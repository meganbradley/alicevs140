---
title: "CMFCRibbonBaseElement::SetCompactMode"
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
ms.assetid: a4fdb2a1-ca48-40ec-89d8-1b268ea3b6ac
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::SetCompactMode
Sets the display size for the ribbon element.  
  
## Syntax  
  
```  
virtual void SetCompactMode(  
   BOOL bCompactMode = TRUE  
);  
```  
  
#### Parameters  
 [in] `bCompactMode`  
 `TRUE` to reduce the display size of the ribbon element; `FALSE` to increase the display size of the ribbon element.  
  
## Remarks  
 The following table summarizes the logic for this method.  
  
|`bCompactMode`|Current ribbon element size|New ribbon element size|  
|--------------------|---------------------------------|-----------------------------|  
|`TRUE`|Compact|No change.|  
|`TRUE`|Intermediate|Compact if it is possible.|  
|`TRUE`|Large|Intermediate if it is possible.|  
|`FALSE`|Compact|Intermediate if it is possible; otherwise large.|  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)